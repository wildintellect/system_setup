# README #
Automate UBUNTU software installation after new OS install, primarily using [Ansible](https://www.ansible.com/)

### Getting Started ###

* [Download and install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html?extIdCarryOver=true&sc_cid=701f2000001OH7YAAW#latest-releases-via-apt-ubuntu)
* Clone repo

### What's included ###

* Common GIS applications
* R
* Other coding tools



### Notes/Hints ###

#### how to run ####
```
sudo su
ansible-playbook -K local.yml --skip-tags "finished"
```

## useful materials ##
* https://www.tricksofthetrades.net/2017/10/02/ansible-local-playbooks/
* https://docs.ansible.com/ansible/latest/index.html
* https://github.com/wtanaka
* https://gist.github.com/perrygeo/7273812
