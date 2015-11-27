S3FS Ansible role for Debian
============================

[FUSE-based file system backed by Amazon S3](https://github.com/s3fs-fuse/s3fs-fuse) for Debian Jessie / Stretch.

Requirements
------------

None.

Role Variables
--------------

### s3mounts

`s3_mounts` is hash list composed:

- `dir`: mount point on system
- `bucket`: bucket name in Amazon
- `owner`: username in system who own the folder (default is root)
- `group`: group name in system who own the folder (default is root)
- `key`: Amazon key ID
- `secret`: Amazon secret IS
- `mount_options`: hash list with key and value (optional)

### Jessie configuration

- `s3_apt_repository`: debian repository used to installed s3fs. If setted to null, this sted is skipped). You should set null only if the respoitory is already configured.

Dependencies
------------

None.

Example Playbook
----------------

See [tests/test.yml](tests/test.yml).

Notes
-----

[s3fs](https://packages.debian.org/stretch/s3fs) is only available from Debian Stretch (current testing). On Debian Jessie, this role uses apt-pinning to install this package.

License
-------

GPLv2

Author Information
------------------

- Twitter: [@hanx\_hx](https://twitter.com/hanxhx_)
