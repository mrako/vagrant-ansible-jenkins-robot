# Trail Provisioning

This is the provisioning library for [Jenkins](https://jenkins-ci.org/) and [Robot Framework](http://robotframework.org/)

## Prerequisites

* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [Ansible](http://docs.ansible.com/intro_installation.html)

## Configuration (Ubuntu 14.04)

    wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
    sudo sh -c 'echo "deb http://download.virtualbox.org/virtualbox/debian trusty contrib" > /etc/apt/sources.list.d/virtualbox.list'
    sudo apt-get update
    sudo apt-get install virtualbox virtualbox-dkms vagrant

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
