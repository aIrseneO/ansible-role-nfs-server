Role Name
=========

Ansible role to deploy a nfs server.

Requirements
------------

None

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

<!-- Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles. -->

Example Playbook
----------------

    - hosts: localhost
      any_errors_fatal: true
      become: true
      roles:
      - role: aIrseneO.nfs-server
        vars:
          nfs_server_exports:
          - export:
            access:
              - hostname: '*'
                options:
                  - 'rw'
                  - 'sync'
                  - 'no_subtree_check'
                  - 'no_root_squash'
            mode: "u=rwx,g=rwx,o=rwx"
            path: "/opt/nfs/test"

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
