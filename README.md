# Ansible LEMP Stack (rhel/debian)
This targets a centos7 and ubuntu vagrant virtual machine.

## Dependencies
You will need Vagrant, Python and Ansible installed to run this.

## Running instructions
Firstly, run ``` vagrant up ```
Wait for the VMs to come up
next you will need to run ``` ansible-playbook -i production site.yml ```