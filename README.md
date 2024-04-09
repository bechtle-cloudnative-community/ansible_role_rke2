ansible_role_rke2
=========

This Role is itended to install and update RKE2.

Tested on: 
 - Debian 11
 - Ubuntu
 - RHEL 9

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
master-node1 rke2_type="server" primary=true
[agent]
agent-node1 rke2_type="agent"
```
playbook example:


```yaml
---
- hosts: all
  vars:
    fqdn: "{{ inventory_name }}.example.com"
  roles:
    - { role: bechtle.rke2 }
```
License
-------

MIT

Author Information
------------------

This role is created by Thomas Geiger @ Bechtle Schweiz AG.

