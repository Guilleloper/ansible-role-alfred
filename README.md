# ANSIBLE ROLE ALFRED

## Description
Ansible role for the Alfred deployment.

(See Alfred repository: https://github.com/Guilleloper/alfred)
<br/><br/>

## Prepare an Ansible environment for deploying the role
Steps to prepare an Ansible environment for deploying the role:
```
$ cd <deployment location>
$ view alfred.yml
~
---
- hosts: alfred
  become: True
  gather_facts: False
  roles:
    - alfred
...
~
$ mkdir roles
$ cd roles/
$ git clone https://github.com/Guilleloper/ansible-role-alfred
$ mv ansible-role-alfred/ alfred/
$ cd ..
```
<br/><br/>
## Deploy Alfred:
```
$ ansible-playbook alfred.yml --diff --check
$ ansible-playbook alfred.yml --diff
```
