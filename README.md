Ansible Role: JetBrains Toolbox
=========

[![Build Status](https://travis-ci.org/webarchitect609/ansible-role-jet-brains-toolbox.svg?branch=master)](https://travis-ci.org/webarchitect609/ansible-role-jet-brains-toolbox)

Installs JetBrains [Toolbox](https://www.jetbrains.com/toolbox/app/) App. 

It downloads and unpacks the tar archive from JetBrains. After the installation is complete,
`jetbrains-toolbox` executable script should be ran manually. It installs the app in `~/.local/share/JetBrains/Toolbox/`
and runs it.    

Requirements
------------

Please, check [Toolbox System requirements](https://toolbox-support.jetbrains.com/hc/en-us/articles/115000978824-What-are-the-system-requirements-for-Toolbox-App-). 


Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    toolbox_version: "1.14.5037"

Which version to install. Please, [check current Toolbox App version](https://www.jetbrains.com/toolbox/download/download-thanks.html) 
or [previous releases](https://toolbox-support.jetbrains.com/hc/en-us/articles/360000048240-Previous-Toolbox-App-releases).
But since it has included auto-update feature, it doesn't really matters which version to use. 


    toolbox_install_dir: "/opt"

Directory to install to.
 

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
         - { role: webarchitect609.jet_brains_toolbox }

*Inside `vars/main.yml`*:

    toolbox_version: "1.14.5037"
    toolbox_install_dir: "/opt"

License
-------

MIT

Author Information
------------------

This role was created in 2019 by Gripinskiy Sergey.
