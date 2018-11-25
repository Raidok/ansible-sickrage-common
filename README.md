ansible-sickrage-common
=====

This role installs and configures [SickRage](https://github.com/SiCKRAGE/SiCKRAGE), an awesome
PVR & episode guide that downloads and manages all your TV shows .

Requirements
------------

This role requires Ansible 1.4 or higher and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows.

    # The install directory
    sickrage_install_dir: '/opt/sickrage'

    # The user under which the service should run
    sickrage_user: 'sickrage'

    # The sickrage GitHub repository to checkout
    sickrage_github_repo: 'https://github.com/SiCKRAGE/SiCKRAGE.git'

Examples
========

1) Install sickrage with default settings

    - hosts: all
      roles:
      - ansible-sickrage-common


2) Install sickrage with customized install path and runas user.

    - hosts: all
      roles:
      - {role:                  'ansible-sickrage-common',
         sickrage_user:        'root',
         sickrage_install_dir: '/usr/local/sickrage'}

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Parv Mihai

