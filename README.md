LVM Partition
=============

[![Build Status](https://travis-ci.org/ome/ansible-role-lvm-partition.svg)](https://travis-ci.org/ome/ansible-role-lvm-partition)
[![Ansible Role](https://img.shields.io/ansible/role/41255.svg)](https://galaxy.ansible.com/ome/lvm_partition/)

Additional LVM logical volumes to be created and mounted.

Existing LVs will be resized.

Role Variables
--------------

These variables must be defined (defaults aren't provided):

- `lvm_vgname`: LVM volume group for the logical volume
- `lvm_lvname`: Logical volume name, use `[A-Aa-z0-9]+` to avoid problems
- `lvm_lvmount`: Where the partition should be mounted
- `lvm_lvsize`: Size of the partition
- `lvm_lvfilesystem`: filesystem for partitions which need to be formatted

Optional variables:

- `lvm_shrink`: Shrink if current size is higher than size requested (default: True)
- `lvm_lvopts`: Logical volume creation options (default: None)

Author Information
------------------

ome-devel@lists.openmicroscopy.org.uk
