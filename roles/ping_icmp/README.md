Role Name
=========

icmp ping role.
This role will test the network reachability of a 'host' via icmp.

Requirements
------------

- ping linux command should be installed
- jc (json c)

Role Variables
--------------

Variables are in the default/main.yml files.
* host_to_ping: ip address to ping
* ping_command: the complete ping command to send ( option '-c n' is mandatory  to stop ping after 'n' icmp echo request )

Dependencies
------------
Dependencies are in the collection readme.

Example Playbook
----------------


```
---
- name: test assert via collection
  hosts: all
  gather_facts: false

  roles:
    - name: assertion PING ICMP
      role: f_pmor.assertions.var_exist_not_null
      vars:
        host_to_ping: "{{ ansible_host }}"
      delegate_to: localhost
```
* : use `delegate_to`: localhost  to ping from the ansible controler.

License
-------

BSD

Author Information
------------------

Philippe Morry (philippe'at'morry.fr)