Role Name
=========

Ansible role for installing nels-galaxy-api (<https://www.github.com/usegalaxy-no/nels-galaxy-api/>)

in requirements:

    - src: https://github.com/usegalaxy-no/ansible-role-nels-galaxy-api.git
      name: usegalaxy-no.nels-galaxy-api

Requirements
------------

Role Variables
--------------

Variables are defined in:

- infrastructure-playbook/env/{test,main}/group_vars/nga.yml
- infrastructure-playbook/env/{test,main}/secret_group_vars/global.vault
- defaults/main.yml

Dependencies
------------

- usegalaxy infrastructure playbook <https://github.com/usegalaxy-no/infrastructure-playbook>
- nels galaxy api <https://github.com/usegalaxy-no/nels-galaxy-api.git>
- ansible
- root access to the main nodes uesgalaxy.no (test or prod)

Usage
------------

1. checkout the infrastucture-playbook
2. follow the instructions <https://usegalaxy-no.readthedocs.io/en/latest/deployment.html>
3. the nga role is included in the requirements.yml and will be installed by ansible-galaxy.
   Step is included in the infrastucture doc.
4. go to the env folder (main or test) and run "ansible-playbook nga.yml"
   nga.yml checks out the nels-galaxy-api and installs it

Example Playbook
----------------

nga.yml in env/test (or env/main for production infra)

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
