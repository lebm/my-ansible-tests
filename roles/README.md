# Roles  

## Roles locations in precedence order (higher to lower)
* ./roles no dir do projeto
* ~/.ansible/roles
* /etc/ansible/roles
* /usr/share/ansible/roles

## [Using Roles (2.9)](https://docs.ansible.com/ansible/2.9/user_guide/playbooks_reuse_roles.html#using-roles)

* Classic
```
---
- hosts: webservers
  roles:
      - common
      - webservers
```

* New
```
---
- hosts: webservers
  tasks:
    - debug:
        msg: "before we run our role"
    - import_role:
        name: example
    - include_role:
        name: example
    - debug:
        msg: "after we ran our role"
```
