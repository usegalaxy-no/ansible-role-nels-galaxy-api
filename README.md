Role Name
=========

Ansible role for installing nels-galaxy-api (https://www.github.com/usegalaxy-no/nels-galaxy-api/)

**Currently broken do not use**


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

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: galaxyserver
      become: true
      vars:
        galaxy_config_file: /srv/galaxy/config/galaxy.yml
        nels_galaxy_key: super-secret-key
        proxy_keys: {'key_for_incoming_proxy1': 'galaxy-1.bioinfo.no',
                     'key_for_incoming_proxy2': 'galaxy-2.bioinfo.no'}


      roles:
        - usegalaxy-no.nels-galaxy-api

License
-------

BSD

Author Information
------------------

Elixir Norway/Bergen University
