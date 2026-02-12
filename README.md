# README #
Automate Ubuntu software installation after new OS install, primarily using [Ansible](https://www.ansible.com/)

These recipes are intended for a single user desktop environment.

### Getting Started ###

#### Install Ansible ####

[Download and install Ansible](https://docs.ansible.com/projects/ansible/latest/installation_guide/installation_distros.html#installing-ansible-on-ubuntu)

```
# Ubuntu PPA repos
sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```

```
# Using Pip doesn't work on Ubuntu anymore
sudo apt-get update
sudo apt-get install python3 -y
sudo easy_install pip3
sudo pip3 install ansible
```

#### Download Repo ####

1. Download this repo and unzip
OR
1. Install git and clone repo

TODO: add a script that can be triggered via wget or curl to download and run the playbooks.

### What's included ###

This is an opnionated list of things I need on some of my machines
See the site.yml file

### Notes/Hints ###
Some of the roles are not single software but related software together to reduce redundancy

#### how to run ####
To run the main playbook
```
ansible-galaxy install -r requirements.yml
ansible-playbook -i inventory -c local -K site.yml
# You will be prompted Become: <sudo password>
```

A second playbook which has software that can only be installed for individual users.
```
ansible-playbook -i inventory -c local -K per_user.yml
```
## useful materials ##
* https://www.tricksofthetrades.net/2017/10/02/ansible-local-playbooks/
* https://docs.ansible.com/ansible/latest/index.html
* https://github.com/wtanaka
* https://gist.github.com/perrygeo/7273812

### Tips ###

* Check your facts
```
ansible localhost -c local -i inventory -m setup
```
* [Debugging](https://docs.ansible.com/ansible/latest/user_guide/playbooks_debugger.html)
