# README #
Automate UBUNTU software installation after new OS install, primarily using [Ansible](https://www.ansible.com/)

### Getting Started ###

#### Install Ansible ####

[Download and install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html?extIdCarryOver=true&sc_cid=701f2000001OH7YAAW#latest-releases-via-apt-ubuntu)

```
#Ubuntu repos
sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```

```
#Using Pip
sudo apt-get update
sudo apt-get install python3 -y
sudo easy_install pip
sudo pip install ansible
```

#### Download Repo ####

1. Download repo and unzip
OR
1. Install git and clone repo

TODO: add a script that can be triggered via wget or curl to download and run the playbooks.

### What's included ###

* Common GIS applications
* R
* Other coding tools

### Notes/Hints ###

#### how to run ####
```
ansible-playbook -i inventory -c local -K site.yml
# You will be prompted Become: <sudo password>
```

## useful materials ##
* https://www.tricksofthetrades.net/2017/10/02/ansible-local-playbooks/
* https://docs.ansible.com/ansible/latest/index.html
* https://github.com/wtanaka
* https://gist.github.com/perrygeo/7273812
