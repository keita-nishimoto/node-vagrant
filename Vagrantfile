# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.ssh.insert_key = false
  config.vm.box = "centos/7"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.provider "virtualbox" do |vm|
    vm.customize ["modifyvm", :id, "--memory", "1024", "--cpus", "2", "--ioapic", "on"]
  end

  config.vm.provision "ansible" do |ansible|
    ansible.limit = "all"
    ansible.inventory_path = "../node-ansible/local"
    ansible.playbook = "../node-ansible/site.yml"
  end
end
