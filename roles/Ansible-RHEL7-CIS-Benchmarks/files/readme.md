Init-Linux
=========

Initialize a RHEL 6 / 7 machine to iLab standard specifications.

Requirements
------------

This role is not guaranteed to function properly on machines that have had OS changes made beyond the Dimension Data base image.

Role Variables
--------------

This role has no variables passed at calling.  The parent playbook should target a machine, or group of machines, and the necessary target information is derived from that.

Dependencies
------------

Expected to be run with **holms.fqdn** in order to set the hostname of the server, but not required.

Example Playbook
----------------

```
---
- hosts: '{{ target }}'
  remote_user: root
  roles:
    - role: holms.fqdn
      fqdn: '{{ short_name }}.{{ domain }}'
      hostname: '{{ short_name }}'
    - role: init-linux
```

Author Information
------------------

Written Q4 2015, Wes Carlton, Deloitte Consulting LLC.
