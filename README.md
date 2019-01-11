# OpenEdx Jenkins for automated testing deployment

This repository contains collection of roles for deploying dockerized environment for OpenEdx Tests Jenkins.

## Prerequisites:

* instance with minimal requirements of 4Gb memory and 12Gb disk space;
* configured network security group allows SSH and HTTP access;
* SSH access for user able to run `sudo` command;
* locally installed [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

## Prepare:

* copy file [inventories/hosts.ini.sample](inventories/hosts.ini.sample) to inventories/hosts.ini
* change `IP_ADDRESS` to IP address of instance;
* `azureuser` to username of system user with `sudo` privileges;
* change 
* copy file [inventories/group_vars/openedx-ci/main.yml.sample](inventories/group_vars/openedx-ci/main.yml.sample) to inventories/group_vars/openedx-ci/main.yml
* change variables according to inline comments

## Run:

```
ansible-playbook -i inventories/hosts.ini install.yml
```

## Verify:

Open with browser http://IP_ADDRESS
