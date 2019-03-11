# -*- mode: ruby -*-
# vi: set ft=ruby :

# vagrant plugin install vagrant-disksize

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.disksize.size = "10GB"

  # If you want to use this system to netboot Raspberry Pi, then uncomment this line
  # config.vm.network "public_network", bridge: 'ask', ip: "10.0.0.1"

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
  end 

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
