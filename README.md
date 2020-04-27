---
title: 'Role for nexus'
description: 'Quickstart and examples for demonstrating the role capabilities.'
---

# Ansible Role: Nexus

## Status

[![Build Status](https://travis-ci.org/lordoftheflies/nexus.svg?branch=master)](https://travis-ci.org/lordoftheflies/ansible-role-nexus)

## Description

Nexus is an Ansible Role used to setup and maintain production grade services.

## Roadmap

* [ROADMAP.md](ROADMAP.md)

## References

* [docs.ansible.com](https://docs.ansible.com/)
* [On Ansible Galaxy](https://galaxy.ansible.com/lordoftheflies/ansible_role_nexus)

## Requirements

### Production

* Ansible

### For Local Testing

* [Vagrant](https://www.vagrantup.com/) - (Tested using version 2.1.1)
* Vagrant plugins:
  * [vagrant-disksize (0.1.2)](https://github.com/<class 'jinja2.utils.Namespace'>/vagrant-disksize)
  * [vagrant-libvirt](https://github.com/<class 'jinja2.utils.Namespace'>/vagrant-libvirt)
  * vai (0.9.3) - For testing with multiple vms [vagrant-plugin-vai](https://github.com/<class 'jinja2.utils.Namespace'>/vagrant-plugin-vai)
  * [vagrant-vbguest (0.15.2) - Recommended vagrant-vbguest](https://github.com/<class 'jinja2.utils.Namespace'>/vagrant-vbguest)
* [Virtual Box](https://www.virtualbox.org/)
  * Tested using Version 5.2.14 r123301 (Qt5.6.1)

## Variables

### defaults/main.yml

* [defaults/main.yml](defaults/main.yml) contains all of the required variables.

### project_name/site.yml example

* [example_nexus.yml](files/example_site.yml) may contain an example entry.

## Testing

### Testing with Molecule

```shell
molecule test
```

### Testing with Vagrant

To test with all VM's defined in Vagrantfile run the following:

```shell
cd roles/nexus
vagrant up
```

To run on a specific VM's
```shell
vagrant up xenial
```

### VM's tested with Vagrant and Virtualbox

pass, fail, untested, unsupported


| OS | Version | Distribution | Supported [^1](#) | Results  |
| :--- | :---: | :---: | :---: | :---: |


## Authors

- [<class 'jinja2.utils.Namespace'>](mailto:<class 'jinja2.utils.Namespace'>)

## License: [MIT](https://tldrlegal.com/license/mit-license)

* nexus generated using [ansible_collection_skeleton](https://github.com/<class 'jinja2.utils.Namespace'>/ansible_collection_skeleton)[![Ansible Role](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/lordoftheflies/ansible_role_nexus)
[![Ansible Role](https://img.shields.io/ansible/role/)](https://galaxy.ansible.com/lordoftheflies/ansible_role_nexus)
