Ansible Role: Sudo v1.0
===

[![Build Status](https://travis-ci.org/mm0/ansible-role-sudo.svg?branch=master)](https://travis-ci.org/mm0/ansible-role-sudo)

An Ansible role that configures sudoers file

Allows you to specify a different list of users with specific sudoers permission string for each host group or within a playbook

See Also: ansible-role-sudo, ansible-role-bash


Requirements
--

Sudo access

Role Variables
--

Available variables are listed below, there are no defaults:

```yml
users:
    ubuntu:
        state: present
        groups:  sudo,ubuntu
        sudo: "ALL=(ALL) NOPASSWD: ALL"
```
Dependencies
--

None 

Example Playbook
--

```yml
- hosts: webservers
  vars:
    users:
        ubuntu:
            state: present
            groups:  sudo,ubuntu
            sudo: "ALL=(ALL) NOPASSWD: ALL"
  roles:
  - ansible-role-sudo
```

License
---------------

BSD-2

Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

[mm0](https://github.com/mm0) on github
