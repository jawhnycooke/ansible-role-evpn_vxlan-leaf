Role Name
=========

Role to help with the configuration of the EVPN/VXLAN leaf switch from Cisco.

Requirements
------------

None

Role Variables
--------------

vlan_list_map:
 - vlan_id: 10
   vxlan_id: 10010
   name: WEB
   ip_address: '10.0.0.1'
   vrf: 'TENANT-A'
   mcast_group: '239.239.239.1'
 - vlan_id: 20
   vxlan_id: 10020
   name: DB
   ip_address: '10.0.1.1'
   vrf: 'TENANT-B'
   mcast_group: '239.239.239.2'
 - vlan_id: 30
   vxlan_id: 10030
   name: DB
   vrf: 'TENANT-A'
   mcast_group: '239.239.239.1'
 - vlan_id: 40
   vxlan_id: 10040
   name: 'TENANT-A'
   vrf: 'TENANT-A'
   l3vni: True
 - vlan_id: 50
   vxlan_id: 10050
   name: 'TENANT-B'
   vrf: 'TENANT-B'
   l3vni: True

Dependencies
------------

None


Example Playbook
----------------
---
To generate the overlay configuration of the leaf switches.
    - hosts: localhost
      roles:
         - { role: rogerscuall.ansible-role-evpn_vxlan-leaf }

License
-------

BSD

Author Information
------------------

Roger Gomez rgomez@presidio.com
