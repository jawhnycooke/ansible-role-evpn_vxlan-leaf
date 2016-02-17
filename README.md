Role Name
=========

Role to help with the configuration of the EVPN/VXLAN leaf switch from Cisco.

Requirements
------------

None

Role Variables
--------------
vlan_list_map: is a list of dictionaries, every element of the list is as follows:
- vlan_id(required): id of the vlan
- vxlan_id(optional): id of the vxlan
- name(required): name of the vlan
- ip_address(optional): ip address of the subnet, if no IP address is provided no SVI is configured
- vrf(required): name of the VRF or Tenant
- mcast_group(required): multicast group for the VTEP.
- l3vni(optional): is only required in the L3VNI.


vxlan_prefix(optional): this number will be added to the vlan_id to find the vxlan_id if no vxlan_id was provided.


any_cast_mac(required): MAC address to support anycast-gateway-mac

Dependencies
------------

None


Example Playbook
----------------
---

    - hosts: localhost
      roles:
         - { role: rogerscuall.ansible-role-evpn_vxlan-leaf }

License
-------

BSD

Author Information
------------------

Roger Gomez rgomez@presidio.com
