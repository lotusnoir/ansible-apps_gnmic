# ansible-apps_gnmic

## Description

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_gnmic-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_gnmic)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_gnmic.svg)](https://github.com/lotusnoir/ansible-apps_gnmic/releases/latest)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_gnmic?color=orange&style=flat)
[![downloads](https://img.shields.io/ansible/role/d/56081)](https://galaxy.ansible.com/lotusnoir/apps_gnmic)
![Ansible Quality Score](https://img.shields.io/ansible/quality/56081)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

Deploy [gnmic](https://github.com/karimra/gnmic) a gnmi CLI client and collector.

## Requirements

none

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_gnmic
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_gnmic


## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

