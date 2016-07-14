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
```
    - hosts: rhel_servers
      roles:
         - { role: mcgill.subscription-manager }
```

TODO
----

 * The tasks need to be refactored to test if a channel is enabled or disabled
   before running the appropriate command.  As it currently stands, it will
   always "change", though with no negative impact on the server.

License
-------

GPL 3

Author Information
------------------

Chris Poupart <chris.poupart@mcgill.ca>
