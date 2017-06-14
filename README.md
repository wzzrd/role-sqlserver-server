Role: role.sqlserver
========

This role installs and configures SQL Server, SQL Server Agent and Always-On Availability Groups ReadOnly Scaling.

Requirements
------------

CentOS7. 

Role Variables
--------------

In the current version, you can specify the following variables:

| Name                  | Default |                                                              |
|-----------------------|---------|--------------------------------------------------------------|
| sa_password           |   ---   | system administrator password for SQL Server install .  |


Dependencies
------------

This package has no dependencies.

License
-------

GPLv2

Author Information
------------------

Created by CNS Technical Group (https://www.cnstechgroup.com/)

Examples
--------

```yaml
---
- name: role.sqlserver-server role 
  hosts: dbservers
  sudo: yes
  roles: 
  - dbserver
  gather_facts: no
  environment:
   SA_PASSWORD: "{{sa_password}}"

```
