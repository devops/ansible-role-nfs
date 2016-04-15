# Ansible Role: nfs

Installs NFS utilities on RedHat/CentOS.

## Requirements

None.

## Role Variables

### `defaults/main.yml`

* `nfs_exports: []`

A list of exports which will be placed in the `/etc/exports` file.
   ```
    Simple example:
        nfs_exports: { "/home/public *(rw,sync,no_root_squash)" }
        nfs_exports:
          - "/home/public1 *(rw,sync,no_root_squash)"
          - "/home/public2 *(rw,sync,no_root_squash)"
   ```

## Dependencies

None.

## Example Playbook

    - hosts: servers
      vars:
        nfs_exports: { "/home/public *(rw,sync,no_root_squash)" }
      roles:
         - nfs

## Author Information

z
