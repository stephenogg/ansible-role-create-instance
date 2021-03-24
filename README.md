# ansible-role-create-instance
Create a nova compute instance using openstack collection commands. Optionally create and attach a new volume
------------
Dependencies
------------

Role Variables
------------
Default variables for all the infomation required to create a new compute instance (nova) on openstack. See see `defaults/main.yml` for the full list.
create_compute_instance: True
Optional variable to create a new volume, if `true`, then the role creates a new CINDER volume called `volume_name` of size `volume_size` on device `device`.
`create_new_volume`: Whether to create a new (2nd) volume along with the compute instance, default `False`.

------------
floating_ip: ''
flavour: 'p4-6gb'
image: Ubuntu-20.04-Focal-x64-2020-12
server_name: 'new_server'
keypair: ''
volume_name: 'new_volume'     
volume_size_gb: 100
device: '/dev/vdb'  # each flavor already has a 20Gb disk mounted on /dev/vda
