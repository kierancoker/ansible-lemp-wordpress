# Ansible LEMP Stack (rhel/debian)
This targets centos (rhel based) or ubuntu (debian based) using a vagrant virtual machine for development/testing.

To apply to a production install, please update the production host file

## Dependencies
You will need Vagrant, Python and Ansible installed to run this.

## Running instructions
- Firstly, run ``` vagrant up ```
- Wait for the VMs to come up
- next you will need to run ``` ansible-playbook -i development site.yml ```

After the Ansible playbook has finished, you can test the installation by heading to

- 192.168.50.6.nip.io
- 192.168.50.7.nip.io
