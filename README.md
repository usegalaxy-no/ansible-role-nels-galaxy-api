ansible-role-nels-galaxy-api
=========

Ansible role for installing nels-galaxy-api (NGA).

NGA new versions are currently hosted at UiB GitLab <https://git.app.uib.no/cbu-dev/nga>. It was formerly hosted in [GitHub](https://www.github.com/usegalaxy-no/nels-galaxy-api/). This version is **obsolete**.

NGA is included in https://github.com/usegalaxy-no/infrastructure-playbook/blob/master/env/common/requirements.yml:

    - src: https://github.com/usegalaxy-no/ansible-role-nels-galaxy-api.git
      name: usegalaxy-no.nels-galaxy-api

Role Variables
--------------

Variables are defined in:

- infrastructure-playbook/env/{test,main}/group_vars/nga.yml
- infrastructure-playbook/env/{test,main}/secret_group_vars/global.vault
- defaults/main.yml

Dependencies
------------

- usegalaxy infrastructure playbook: <https://github.com/usegalaxy-no/infrastructure-playbook>
- NGA:  <https://git.app.uib.no/cbu-dev/nga>. Please note that previous NGA version hosted in [GitHub](https://www.github.com/usegalaxy-no/nels-galaxy-api/) is **obsolete** and must not be used anymore.
- ansible
- root access to the main nodes usegalaxy.no (test or prod)

Usage
------------

1. Checkout the infrastucture-playbook
2. Follow the instructions <https://usegalaxy-no.readthedocs.io/en/latest/deployment.html>
3. The NGA role is included in the requirements.yml and will be installed by ansible-galaxy.
   Step is included in the infrastructure doc.
4. Go to the env folder (main or test) and run "ansible-playbook nga.yml"
   nga.yml checks out the NGA and installs it.

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
