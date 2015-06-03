# Trail Provisioning

This is the provisioning library for [Jenkins](https://jenkins-ci.org/) and [Robot Framework](http://robotframework.org/)

## Prerequisites

* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [Ansible](http://docs.ansible.com/intro_installation.html)

## Playbooks

* Base
* Apache
* Security
* Java
* Jenkins
* Robot
* Node
* PhantomJS

## Usage

### Provisioning

    vagrant destroy -f && vagrant up

### Accessing

[Jenkins (localhost:8888)](http://localhost:8888)

Through SSH

        ssh deploy@localhost -p 2222

### Deploying Application

    ansible-playbook provisioning/playbook.yml -i <your hosts file>

### Listing virtualboxes

    VBoxManage list vms
