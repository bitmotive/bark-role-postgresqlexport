BARK: POSTGRESQLEXPORT
=========

Automate a PostgreSQL database backup

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

**POSTGRESQLEXPORT_DB_NAME**:

The name of the database to export.

**POSTGRESQLEXPORT_DB_USER**:

The PostgreSQL who will connect to the databse.

**POSTGRESQLEXPORT_DB_USER_PASSWORD**:

The password of the PostgreSQL user.

**POSTGRESQLEXPORT_DESTINATION_FOLDER**:

Where to place the exported SQL file on the machine running Ansible.


Dependencies
------------

Tested on Linux systems. Assumes ability to pg_dump from target host shell.

License
-------

MIT

Author Information
------------------

A Bitmotive Project: Build. Incubate. Train.
https://bitmotive.com 
