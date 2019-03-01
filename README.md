Role Name
=========

Role for configuring users and hostname, and updating system packages on an ubuntu machine.

Requirements
------------

This role assumes that you have Ubuntu 18.04 installed and accessible via ssh.

Role Variables
--------------

hostname: String specifying the hostname to set for the system.
users: array of users to create on the target system. Users consist of a name, groups, password, and salt. If the password for a user is not specified, the user will not be allowed to log in, but will still be created.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: ubuntu_base
           vars:
             hostname: somehost
             users:
              - name: human
                groups: [ users, sudo ]
                password: 'supersecret'
                salt: 'salty'
              - name: service
                groups: [ services ]



License
-------

MIT
