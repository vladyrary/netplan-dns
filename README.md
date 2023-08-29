Role Name
=========

This role changes the DNS addresses of the network interface

Requirements
------------

This role is limited to:

Ubuntu 18.04
Ubuntu 20.04
Ubuntu 22.04

Role Variables
--------------

dns_servers --- list of IPs for DNS servers, default ['8.8.8.8', '1.1.1.1']

Dependencies
------------

None

Example Playbook
----------------

   ---
- name: Playbook to run role netplan-dns
  hosts: servers
  become: true
  vars:
    interfaces:
    - interface: ens3
      dns:
        nameservers:
        - "8.8.8.8"
        - "1.1.1.1"
  roles:
     - role: '/root/roles/netplan-dns'

License
-------

BSD

Author Information
------------------

t.me/lambtalk

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
# netplan-dns
