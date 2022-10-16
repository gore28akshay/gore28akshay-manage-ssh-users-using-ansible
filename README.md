### Ansible to manage ssh users in infrastruture ###
**Folder Structure**
```
.
├── inv
│   ├── production
│   │   ├── dba
│   │   ├── group_vars
│   │   │   ├── all
│   │   │   │   └── vars.yaml
│   │   │   ├── dba.yaml
│   │   │   ├── jumpbox.yaml
│   │   │   ├── mongo.yaml
│   │   │   ├── redis.yaml
│   │   │   └── web.yaml
│   │   ├── infra
│   │   └── web
│   └── sit
├── playbooks
│   ├── manage_ssh_users
│   │   ├── tasks
│   │   │   └── main.yaml
│   │   └── templates
│   │       └── etc
│   │           └── sudoers
│   ├── net_tools
│   └── site.yaml
└── sshkeys
    ├── user_1.pub
    └── user_2.pub
```

#### How to use this repo ####
1. Add public of users to be managed in sshkeys folder.
2. Add usernames in respective files in group_vars folder
3. Sample command to run playbook
```ansible-playbook -i inv/prod/infra playbooks/site.yaml```
