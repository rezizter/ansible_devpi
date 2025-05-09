Role Name
=========

This role will allow you to install devpi server on a RedHat based server.

Requirements
------------

Python >=3.6.
Ansible >=2.9.

Role Variables
--------------

* devpi_port

  The port number on which the devpi server should listen. Defaults to
  3141. Always listens on localhost.

* devpi_wheelhouse

  The directory used for pip's wheelhouse cache. Defaults to
  ~/.pip/wheelhouse.

* devpi_version
  Set the version of devpi-server that you need.

Dependencies
------------

RedHat based server with python3 installed.

Example Playbook
----------------

```bash
    - hosts: servers
    - name: Include role devpi
      ansible.builtin.include_role:
        name: rezizter.ansible-devpi
        apply:
          tags:
            - devpi
      tags:
        - devpi
```

License
-------

BSD

Author Information
------------------

Rezizter
