i3-wm 
=========

configures i3 just the way I like it

Requirements
------------

you need to be on an debian based system

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

nope

Example Playbook
----------------

```
- hosts: localhost
  connection: local
  gather_facts: false

  vars:
    user_dir: /home/conto

  roles:
    - geerlingguy.mac.homebrew
    - geerlingguy.mac.mas
```

License
-------

BSD

Author Information
------------------

Constantijn van Hartesveldt <constantijn@vanhartesveldt.nl> 