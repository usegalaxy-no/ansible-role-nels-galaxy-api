Role Name
=========

Ansible role for installing tos-api (https://www.github.com/usegalaxy-no/tos-api/)

in requirements:

    - src: https://github.com/usegalaxy-no/ansible-role-tos-api.git
      name: usegalaxy-no.tos-api


Requirements
------------


Role Variables
--------------

All variables are defined in the defaults/main.yml file. However *galaxy_config_file* needs to be sat, pointing to the config file for the galaxy it is to interact with 


Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: galaxyserver
      become: true
      vars:
        galaxy_config_file: /srv/galaxy/config/galaxy.yml
      roles:
        - usegalaxy-no.tos-api

License
-------

BSD

Author Information
------------------

Elixir Norway/Bergen University
