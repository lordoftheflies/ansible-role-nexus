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

Setup LXD:

```shell script
sudo apt install acl autoconf dnsmasq-base git golang libacl1-dev libcap-dev liblxc1 liblxc-dev libtool libudev-dev libuv1-dev make pkg-config rsync squashfs-tools tar tcl xz-utils ebtables
sudo apt install curl gettext jq sqlite3 uuid-runtime bzr socat
sudo apt install lxd lxd-client
lxd init
lxc launch ubuntu:18.04 first
echo "root:1000000:65536" | sudo tee -a /etc/subuid /etc/subgid
sudo -E LD_LIBRARY_PATH=$LD_LIBRARY_PATH $GOPATH/bin/lxd --group sudo
```



Setup Molecule:

```shell script
virtualenv --python=/usr/bin/python3.7 env
source ./env/bin/activate
pip install molecule[lint] molecule[docker] vagrant docker
```

Setup Vagrant:

```shell script
vagrant plugin install vagrant-disksize
vagrant plugin install vai
vagrant plugin install vagrant-libvirt
```



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
