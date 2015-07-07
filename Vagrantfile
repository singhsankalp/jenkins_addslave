# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision/playbook.yml"
    ansible.sudo = true
    ansible.inventory_path = "provision/ansible_hosts"
    ansible.verbose = "vvvv"
  end

# config.vm.define "jenkins" do |worker|
#   worker.vm.box = "chef/centos-6.5"
#   worker.vm.network :private_network, ip: "192.168.6.25"
#   worker.vm.hostname = "jenkins"
# end

  config.vm.define "jenkinsSlave" do |worker|
    worker.vm.box = "chef/centos-6.5"
    worker.vm.network :private_network, ip: "192.168.6.26"
    worker.vm.hostname = "jenkinsSlave"
  end

end
