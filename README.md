BARK: MYSQLEXPORT
=========

Automate a MySQL database backup

Requirements
------------

All roles in the Bitmotive Ansible Role Kit are configuration driven.

Customize this role by providing environment variables in either your
shell environment, host specific in group_vars/, or at the CLI when
prompted at runtime. 

Role Variables
--------------

**POSTGRESQLEXPORT_DB_HOST**:

The hostname or IP address of the PostgreSQL server.

**POSTGRESQLEXPORT_DB_PORT**:

The port number on which the PostgreSQL server is listening (default: 5432).

**MYSQLEXPORT_DB_NAME**:

The name of the database to export.

**MYSQLEXPORT_DB_USER**:

The MySQL who will connect to the databse.

**MYSQLEXPORT_DB_USER_PASSWORD**:

The password of the MySQL user.

**MYSQLEXPORT_DESTINATION_FOLDER**:

Where to place the exported SQL file on the machine running Ansible.


Dependencies
------------

If you connect to a remote host as a user other than root and 
attempt to use `become: yes` along with `become_user: postgres` you are
likely to encounter known issues with Ansible's privilege escalation
in regard to temp files:

https://docs.ansible.com/ansible-core/2.15/playbook_guide/playbooks_privilege_escalation.html#risks-of-becoming-an-unprivileged-user

One solution for this is to place lines such as the following in your ansible.cfg: 
```
remote_tmp = /tmp/ansible-remote
local_tmp = /tmp/ansible-local
allow_world_readable_tmpfiles = True
remote_tmp_dir_mode = 0777
```



License
-------

MIT

Author Information
------------------

A Bitmotive Project: Build. Incubate. Train.
https://bitmotive.com 
