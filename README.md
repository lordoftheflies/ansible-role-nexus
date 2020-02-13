# Ansible Role: Nexus Repository Manager

## Status

[![Build Status](https://travis-ci.org/lordoftheflies/role_nexus.svg?branch=master)](https://travis-ci.org/lordoftheflies/role_nexus)

## Supported platforms

[![Platforms](http://img.shields.io/badge/platform-ubuntu_19.10-purple.svg?style=flat)](#)

[![Platforms](http://img.shields.io/badge/platform-ubuntu_18.10-purple.svg?style=flat)](#)

## Description

ansible-role-nexus is an Ansible role used to...

## Roadmap

* [ROADMAP.md](ROADMAP.md)

## References

* [docs.ansible.com](https://docs.ansible.com/)

## Requirements

### Production

* Ansible

### For Local Testing

* [Vagrant](https://www.vagrantup.com/) - (Tested using version 2.1.1)
* Vagrant plugins:
  * [vagrant-disksize (0.1.2)](https://github.com/lordoftheflies/vagrant-disksize)
  * vagrant-vbguest (0.15.2) - Recommended [vagrant-vbguest](https://github.com/lordoftheflies/vagrant-vbguest)
  * vai (0.9.3) - For testing with multiple vms [vagrant-plugin-vai](https://github.com/lordoftheflies/vagrant-plugin-vai) 
* [Virtual Box](https://www.virtualbox.org/)
  * Tested using Version 5.2.14 r123301 (Qt5.6.1) 

## Variables

### defaults/main.yml

* [defaults/main.yml](defaults/main.yml) contains all of the required variables.

### project_name/site.yml example

* [example_ansible-role-nexus.yml](files/example_site.yml) may contain an example entry.

## Testing

Setup test environment:

```shell script
virtualenv --python=/usr/bin/python3.7 env
source ./env/bin/activate
pip install molecule
```

To test with all VM's defined in Vagrantfile run the following:

```shell
cd roles/lordoftheflies.role_nexus
vagrant up
```

To run on a specific VM's
```shell
vagrant up xenial
```

### VM's tested with Vagrant and Virtualbox

pass, fail, untested

| Distribution | Results  |
| ------------ | -------- |
| precise      | untested |
| trusty       | untested |
| xenial       | untested |
| bionic       | untested |
| CentOS 6     | untested |
| CentOS 7     | untested |

## Authors and License

- [lordoftheflies](mailto:laszlo.hegedus@cherubits.hu)

## License

[MIT](https://tldrlegal.com/license/mit-license)

* ansible-role-ansible-role-nexus generated using [galaxy-role-skeleton](https://github.com/cjsteel/galaxy-role-skeleton)
