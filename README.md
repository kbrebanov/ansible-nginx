nginx
=====

[![Ansible Role](https://img.shields.io/ansible/role/4966.svg)](https://galaxy.ansible.com/list#/roles/4966)

Installs nginx.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                            | Default                  | Description |
|---------------------------------|--------------------------|-------------|
| nginx_version                   | 1.8.0                    | Version of nginx to install                   |
| nginx_daemon_args               | ""                       | Additional options that are passed to nginx
| nginx_error_log_level           | warn                     | Level of logging
| nginx_worker_priority           | 0                        | Defines the scheduling priority for worker processes |
| nginx_worker_processes          | 1                        | Defines the number of worker processes


Dependencies
------------

None

Example Playbook
----------------

Install nginx
```
- hosts: all
  roles:
    - { role: kbrebanov.nginx }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
