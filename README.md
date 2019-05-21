Enhancements of the original openmicroscopy/ansible-role-lvm-parition code

LVM Partition
=============

Additional LVM logical volumes to be created and mounted.

Existing LVs will be resized.

Role Variables
--------------

Default variables:

- `lvm_mount_dump`: 1 
- `lvm_mount_opts`: defaults
- `lvm_mount_passno`: 2

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

info@safeincyberspace.com
