Borg Backup-Server
=========

This ansible role sets up the configuratino for my backup server based on borg
backup. This includes authentication via SSH aswell as the correct settings to
server the repostitory.

Requirements
------------

This role depends on password-store for setting the correct SSH-keys for
authentiauthentication. Make sure to insert the correct keys in your
password-store repostitory or adapt the paths used in the role to your liking.

Role Variables
--------------

| Variable         | Default     | Description                      |
|------------------|-------------|----------------------------------|
| borg_remote_path | /mnt/backup | The mount path of the repository |

Dependencies
------------

This role depends on a working SSH-server. You can use my `ansible-openssh` role
or set it up yourself.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
    - ansible-backup-server
```

License
-------

BSD

Author Information
------------------

https://pablo.tools
