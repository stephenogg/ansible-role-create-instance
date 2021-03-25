[![Ansible Role](https://img.shields.io/static/v1?label=role&message=sco.create_instance&color=blue)](https://github.com/steveo-sudo/ansible-role-create_instance/archive/0.1.0.tar.gz)

# ansible-role-create-instance
Create a nova compute instance using openstack collection commands. Optionally create and attach a new volume

Dependencies
------------
Requires the `openstack.cloud` community collection to be available `ansible-galaxy collection install openstack.cloud`
NOTE: Installing collections with ansible-galaxy is only supported in ansible 2.9+

Role Variables
------------
Default variables for all the infomation required to create a new compute instance (nova) on openstack. See see `defaults/main.yml` for the full list.
- `create_compute_instance: True`
- `create_new_volume`: Whether to create a new (2nd) volume along with the compute instance, default `False`.
  Optional variable to create a new volume, if `true`, then the role creates a new CINDER volume called `volume_name` of size `volume_size` on device `device`.
- `floating_ip: ''` Passing an empty string creaets an instance with only an internal IP address.
- `flavour: 'p4-6gb'` Choices for arbutus are p1-1.5gb, p2-3gb, p4-6gb, p8-12gb
- `image: Ubuntu-20.04-Focal-x64-2020-12` Images for CentOS7 CentOS8 Ubuntu18, Debian10 & Fedora32 available.
- `server_name: 'new_server'`
-  `keypair: ''` 
-  `volume_name: 'new_volume'`
-  `volume_size_gb: 100` New Volume size in Gb
-  `device: '/dev/vdb'` Every flavor already has a 20Gb disk mounted on /dev/vda`
------------





     


