# -*- mode: ruby -*-
# vi: set ft=ruby :

API_VERSION = "2"
DOMAIN      = "wordpress"
PRIVATE_KEY = "~/.ssh/id_rsa"
PUBLIC_KEY  = '~/.ssh/id_rsa.pub'
CENTOS_IP   = '192.168.50.6'
CENTOS_BOX  = 'centos/7'
UBUNTU_IP   = '192.168.50.7'
UBUNTU_BOX  = 'generic/ubuntu1704'

Vagrant.configure(API_VERSION) do |config|

  config.vm.define "centos" do |centos|
      centos.vm.box = CENTOS_BOX
      centos.vm.network "private_network", ip: CENTOS_IP
      centos.vm.host_name = CENTOS_IP + '.' + DOMAIN
      centos.ssh.insert_key = false
      centos.ssh.private_key_path = [PRIVATE_KEY,
      "~/.vagrant.d/insecure_private_key"]
      centos.vm.provision "file", source: PUBLIC_KEY, destination:
      "~/.ssh/authorized_keys"

      centos.vm.provider "virtualbox" do |v|
        v.memory = "2024"
        v.cpus = "2"
      end

      centos.vm.provider "vmware_fusion" do |v|
        v.vmx["memsize"] = "2024"
        v.vmx["numvcpus"] = "2"
      end
  end

  config.vm.define "ubuntu" do |ubuntu|
      ubuntu.vm.box = UBUNTU_BOX
      ubuntu.vm.network "private_network", ip: UBUNTU_IP
      ubuntu.vm.host_name = UBUNTU_IP + '.' + DOMAIN
      ubuntu.ssh.insert_key = false
      ubuntu.ssh.private_key_path = [PRIVATE_KEY,
      "~/.vagrant.d/insecure_private_key"]
      ubuntu.vm.provision "file", source: PUBLIC_KEY, destination:
      "~/.ssh/authorized_keys"

      ubuntu.vm.provider "virtualbox" do |v|
        v.memory = "2024"
        v.cpus = "2"
      end

      ubuntu.vm.provider "vmware_fusion" do |v|
        v.vmx["memsize"] = "2024"
        v.vmx["numvcpus"] = "2"
      end
  end

end