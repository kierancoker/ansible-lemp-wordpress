# Ansible LEMP Stack (rhel/debian)
This targets centos (rhel based) or ubuntu (debian based) using a vagrant virtual machine for development/testing.

To apply to a production install, please update the production host file

**NOTE** this installs a wordpress instance purely as an example of the LEMP are installed and correctly working.

## Dependencies
You will need Vagrant, Python and Ansible installed to run this.

## Running instructions for development
- Firstly, run ``` vagrant up ```
- Wait for the VMs to come up
- next you will need to run ``` ansible-playbook -i development site.yml ```

After the Ansible playbook has finished, you can test the installation by heading to

- 192.168.50.6.nip.io
- 192.168.50.7.nip.io

## Running instructions for production
- Updated production hosts file with your production server ip/hostname
- Ensure you have keyless ssh access with a specified user
- run the following ``` ansible-playbook -i production site.yml ```

After the playbook has finished, head on over to the specified ip/hostname in your browser to test the wordpress instance was successfully installed.
