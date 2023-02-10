ansible_role_rke2
=========

This Role is itended to Install and update RKE2. 
Tested with molcule on: 
 - Debian 11

Requirements
------------

You need at least 2 Nodes. One for the Control plane and as Primary Master and one as Agent(worker), as this is tested with the role.

Role Variables
--------------

Please refer to defaults/main.yml


Example Playbook
----------------

Inventory example:

```INI
[server]
master-node1 rke2_type="server"

[agent]
agent-node1 rke2_type="agent"
```

- hosts: all
  roles:
    - { role: bechtle.rke2 }

License
-------

MIT

Author Information
------------------

This role is created by Thomas Geiger @ Bechtle Schweiz AG.

