![Ansible Lint](https://github.com/johanneskastl/ansible-role-set_hostname/workflows/Ansible%20Lint/badge.svg)

set_hostname
=========

Set a node's hostname in /etc/hostname. Uses the FQDN by default, with the domain part configurable via variable.
Reboot the node afterwards for all the changes to take effect.

Requirements
------------

None.

Role Variables
--------------

`domain_name`: Specify the domain part of the FQDN.

Dependencies
------------

Needs the reboot role to trigger a reboot after setting the hostname. This avoids funny corner cases with hostnames not being set properly.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: johanneskastl.set_hostname, domain_name: 'example.org' }

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
