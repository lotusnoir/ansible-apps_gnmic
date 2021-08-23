# Ansible Role: ansible-apps_gnmic

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_gnmic.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_gnmic)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_gnmic-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_gnmic)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_gnmic?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_gnmic)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_gnmic.svg)](https://github.com/lotusnoir/ansible-apps_gnmic/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_gnmic&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_gnmic)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_gnmic&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_gnmic)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_gnmic&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_gnmic)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_gnmic&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_gnmic)


Deploy [gnmic](https://github.com/danielqsj/gnmic/) to expose kafka metrics to prometheus.

## Role variables

| Name                           | Default Value  | Description                        |
| ------------------------------ | -------------- | -----------------------------------|
| `gnmic_version`       | 0.13.0         | gnmic version |
| `gnmic_temp_dir`      | /tmp           | temporary directory to uncompress package |
| `gnmic_install_dir`   | /usr/local/bin | directory to install binary |
| `gnmic_force_install` | false          | force install variable |
| `gnmic_port`          | 9150           | port to expose prometheus metrics |

## Examples

	---
	- hosts: apps_gnmic
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_gnmic
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## Prometheus rules

TODO

## Grafana dashboard

A sample dashboard is available here: [https://grafana.com/grafana/dashboards/13572](https://grafana.com/grafana/dashboards/13572)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
