Ansible Role: JetBrains Toolbox
===============================
[![Build Status](https://github.com/webarchitect609/ansible-role-jet-brains-toolbox/workflows/build/badge.svg?branch=master)](https://github.com/webarchitect609/ansible-role-jet-brains-toolbox/actions?query=workflow%3Abuild)
[![Latest version](https://img.shields.io/github/v/tag/webarchitect609/ansible-role-jet-brains-toolbox?sort=semver)](https://github.com/webarchitect609/ansible-role-jet-brains-toolbox/releases)
[![Downloads](https://img.shields.io/ansible/role/d/39614)](https://galaxy.ansible.com/webarchitect609/jet_brains_toolbox)
[![License](https://img.shields.io/github/license/webarchitect609/ansible-role-jet-brains-toolbox)](LICENSE.md)
[![More stuff from me](https://img.shields.io/badge/galaxy-webarchitect609-000)](https://galaxy.ansible.com/webarchitect609)

Installs JetBrains [Toolbox App](https://www.jetbrains.com/toolbox/app/). 

It downloads and unpacks the tar archive from JetBrains. After the installation is complete,
`jetbrains-toolbox` executable script should be ran manually. It installs the app in `~/.local/share/JetBrains/Toolbox/`
and runs it.

Requirements
------------

Please, check [Toolbox System requirements](https://toolbox-support.jetbrains.com/hc/en-us/articles/115000978824-What-are-the-system-requirements-for-Toolbox-App-). 


Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    toolbox_version: "1.21.9712"

Which version to install. Please, [check current Toolbox App version](https://www.jetbrains.com/toolbox/download/download-thanks.html) 
or [previous releases](https://toolbox-support.jetbrains.com/hc/en-us/articles/360000048240-Previous-Toolbox-App-releases).
But since it has included auto-update feature, it doesn't really matters which version to use. 


    toolbox_install_dir: "/opt"

Directory to install to.

    toolbox_install_for_user: ""

User, who will use the application.

    inotify_max_user_watches: "524288"
    
Value for [Inotify Watches Limit](https://youtrack.jetbrains.com/articles/IDEA-A-2/Inotify-Watches-Limit?_ga=2.156569083.1588360972.1630133506-996241065.1624703636)
to be set via `sysctl`. 

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: webarchitect609.jet_brains_toolbox }
      vars:
        toolbox_version: "1.21.9712"
        toolbox_install_dir: "/opt"
        toolbox_install_for_user: "yourusername"

License & Author Information
-------
[BSD-3-Clause](LICENSE.md)
