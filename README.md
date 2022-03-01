Role Name
=========

Ansible role for installing nels-galaxy-api (https://www.github.com/usegalaxy-no/nels-galaxy-api/)


in requirements:

    - src: https://github.com/usegalaxy-no/ansible-role-nels-galaxy-api.git
      name: usegalaxy-no.nels-galaxy-api



Requirements
------------


Role Variables
--------------

All variables are defined in the defaults/main.yml file. However *galaxy_config_file* needs to be sat, pointing to the config file for the galaxy it is to interact with 


Dependencies
------------


Example Playbook
----------------

Install the role into the infrastructur playbook role dir infrastructure-playbook/env/common/roles/

Create the nga.yml in env/test (or env/main for production infra)


    - hosts: galaxyserver
      vars_files:
        - secret_group_vars/global.vault
        - group_vars/global.yml
        - group_vars/env.yml
        - group_vars/nga.yml
      become: true
      roles:
        - usegalaxy-no.nels-galaxy-api

License
-------

BSD

Author Information
------------------

Elixir Norway/Bergen University
