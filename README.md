[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

nginx
=====

[![Build Status](https://travis-ci.org/kbrebanov/ansible-nginx.svg?branch=master)](https://travis-ci.org/kbrebanov/ansible-nginx)

Installs nginx.

Requirements
------------

This role requires Ansible 1.9 or higher.

Role Variables
--------------

| Name                            | Default                  | Description                                                                                                                                                        |
|:--------------------------------|:-------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nginx_version                   | 1.10.1                   | Version of nginx to install                                                                                                                                        |
| nginx_daemon_args               | ""                       | Additional options that are passed to nginx                                                                                                                        |
| nginx_error_log_level           | warn                     | Level of logging                                                                                                                                                   |
| nginx_worker_priority           | 0                        | Defines the scheduling priority for worker processes                                                                                                               |
| nginx_worker_processes          | 1                        | Defines the number of worker processes                                                                                                                             |
| nginx_events_worker_connections | 1024                     | Sets the maximum number of simultaneous connections that can be opened by a worker process.                                                                        |
| nginx_http_default_type         | application/octet-stream | Defines the default MIME type of a response.                                                                                                                       |
| nginx_http_keepalive_timeout    | 65                       |                                                                                                                                                                    |
| nginx_http_sendfile             | 'on'                     | Enables or disables the use of sendfile().                                                                                                                         |
| nginx_http_tcp_nopush           | 'off'                    | Enables or disables the use of the TCP_NOPUSH socket option on FreeBSD or the TCP_CORK socket option on Linux. The options are enabled only when sendfile is used. |
| nginx_gzip                      | 'off'                    | Enables or disables gzipping of responses.                                                                                                                         |

Dependencies
------------

None

Example Playbook
----------------

Install nginx
```yaml
- hosts: all
  roles:
    - kbrebanov.nginx
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
