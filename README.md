---
title: 'Role for nexus'
description: 'Ansible Role for setup Nexus Repository Manager.'
---

# Ansible Role: Nexus

Ansible Role for setup Nexus Repository Manager.

## Status

[![Build Status](https://travis-ci.org/lordoftheflies/ansible-role-nexus.svg?branch=master)](https://travis-ci.org/lordoftheflies/ansible-role-nexus)

[![Version](https://img.shields.io/github/v/tag/lordoftheflies/ansible-role-nexus?sort=semver)](https://github.com/lordoftheflies/ansible-role-nexus/releases)

![GitHub Release Date](https://img.shields.io/github/release-date/lordoftheflies/ansible-role-nexus)

[![time tracker](https://wakatime.com/badge/github/lordoftheflies/ansible-role-nexus.svg)](https://wakatime.com/badge/github/lordoftheflies/ansible-role-nexus)

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

## Variables

* [defaults/main.yml](defaults/main.yml) contains all of the required variables.

## Testing

### For Local Testing

* [Vagrant](https://www.vagrantup.com/) - (Tested using version 2.1.1)
* Vagrant plugins:
  * [vagrant-disksize (0.1.2)](https://github.com/lordoftheflies/vagrant-disksize)
  * [vagrant-libvirt](https://github.com/lordoftheflies/vagrant-libvirt)
  * vai (0.9.3) - For testing with multiple vms [vagrant-plugin-vai](https://github.com/lordoftheflies/vagrant-plugin-vai)
  * [vagrant-vbguest (0.15.2) - Recommended vagrant-vbguest](https://github.com/lordoftheflies/vagrant-vbguest)
* [Virtual Box](https://www.virtualbox.org/)
  * Tested using Version 5.2.14 r123301 (Qt5.6.1)

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

## Authors

* This role was created in 2014 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
* Role upgraded in 2019 by [László Hegedűs](mailto:laszlo.hegedus@cherubits.hu), founder of [Cherubits LLC](https://portal.cherubits.hu)

## License

[Apache 2.0](https://tldrlegal.com/license/apache-license-2.0-(apache-2.0))

**NOTE**: Role generated using [ansible-role-skeleton](https://github.com/lordoftheflies/ansible-role-skeleton)
