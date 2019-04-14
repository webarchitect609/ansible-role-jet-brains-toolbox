Ansible Role: JetBrains Toolbox
=========

Installs JetBrains [Toolbox](https://www.jetbrains.com/toolbox/app/)

Requirements
------------

Check JetBrains Toolbox [System requirements](https://www.jetbrains.com/toolbox/app/#systemRequirements)


Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    toolbox_version: "1.14.5037"

Which [version/build](https://toolbox-support.jetbrains.com/hc/en-us/articles/360000048240-Previous-Toolbox-App-releases) to install.

    toolbox_install_dir: "/opt"

Directory to install to.

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
         - { role: webarchitect609.jet-brains-toolbox }

*Inside `vars/main.yml`*:

    toolbox_version: "1.14.5037"
    toolbox_install_dir: "/opt"


License
-------

MIT

Author Information
------------------

This role was created in 2019 by Gripinskiy Sergey.
