# README.md

# Ansible Role: Sudo v1.0

An Ansible role that configures sudoers file

Allows you to specify a different list of users with specific sudoers permission string for each host group or within a playbook

See Also: ansible-role-sudo, ansible-role-bash

![travis-ci](https://travis-ci.org/mm0/ansible-role-sudo.svg?branch=master)

## Requirements

Sudo access

## Role Variables

Available variables are listed below, there are no defaults:

		users:
			ubuntu:
				state: present
				groups:  sudo,ubuntu
				sudo: "ALL=(ALL) NOPASSWD: ALL"

## Dependencies

None 

## Example Playbook

    - hosts: webservers
      vars:
				users:
					ubuntu:
						state: present
						groups:  sudo,ubuntu
						sudo: "ALL=(ALL) NOPASSWD: ALL"
      roles:
      - ansible-role-sudo

## License

MIT


Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

mm0 on github
