Ansible Role: JetBrains Toolbox
===============================

[![Build Status](https://github.com/webarchitect609/ansible-role-jet-brains-toolbox/actions/workflows/build.yml/badge.svg)](https://github.com/webarchitect609/ansible-role-jet-brains-toolbox/actions/workflows/build.yml)
[![Latest version](https://img.shields.io/github/v/tag/webarchitect609/ansible-role-jet-brains-toolbox?sort=semver)](https://github.com/webarchitect609/ansible-role-jet-brains-toolbox/releases)

[![Downloads](https://img.shields.io/ansible/role/d/webarchitect609/jet_brains_toolbox)](https://galaxy.ansible.com/ui/standalone/roles/webarchitect609/jet_brains_toolbox)
[![License](https://img.shields.io/github/license/webarchitect609/ansible-role-jet-brains-toolbox)](LICENSE.md)
[![More stuff from me](https://img.shields.io/badge/galaxy-webarchitect609-000)](https://galaxy.ansible.com/ui/standalone/namespaces/7493/)

Installs JetBrains [Toolbox App](https://www.jetbrains.com/toolbox/app/). 

It downloads and unpacks the tar archive from JetBrains. After the installation is complete,
`jetbrains-toolbox` executable script should be run manually. It installs the app in `~/.local/share/JetBrains/Toolbox/`
and runs it.

Requirements
------------

Please, check [Toolbox System requirements](https://toolbox-support.jetbrains.com/hc/en-us/articles/115000978824-What-are-the-system-requirements-for-Toolbox-App-). 


Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - { role: webarchitect609.jet-brains-toolbox }
  vars:
    toolbox_version: "2.2.1.19765"
```

License & Author Information
----------------------------

[BSD-3-Clause](LICENSE.md)
