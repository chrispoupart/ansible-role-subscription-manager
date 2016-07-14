Role Name
=========

Enable or disable Red Hat repositories using "subscription-manager"

Role Variables
--------------
```
rhsub_repos:
  - name: rhel-7-server-extras-rpms     # wildcard or repo name
    state: enable                       # enable or disable      
```

Example Playbook
----------------

    - hosts: rhel_servers
      roles:
         - { role: mcgill.subscription-manager }

License
-------

GPL 3

Author Information
------------------

Chris Poupart <chris.poupart@mcgill.ca>
