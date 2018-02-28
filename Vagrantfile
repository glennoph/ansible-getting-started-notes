# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.synced_folder ".", "/vagrant", disabled: true

  # ansible control node
  config.vm.define :control, primary: true do |control_config|
    control_config.vm.box = "geerlingguy/centos7"
    control_config.vm.hostname = "control"
    control_config.vm.network "public_network", ip: "10.0.3.10"
    control_config.vm.provider "virtualbox" do |v|
      v.memory = 1024
      v.cpus = 2
    end    
  end

  # centos client
  config.vm.define :centos do |centos_config|
    centos_config.vm.box = "geerlingguy/centos7"
    centos_config.vm.hostname = "centos"
    centos_config.vm.network "public_network", ip: "10.0.3.11"
    centos_config.vm.provider "virtualbox" do |v|
      v.memory = 800
      v.cpus = 2
    end    
  end
  
  # ubuntu client
  config.vm.define :ubuntu do |ubuntu_config|
    ubuntu_config.vm.box = "ubuntu/xenial64"
    ubuntu_config.vm.hostname = "ubuntu"
    ubuntu_config.vm.network "public_network", ip: "10.0.3.12"
    ubuntu_config.vm.provider "virtualbox" do |v|
      v.memory = 800
      v.cpus = 2
    end  
  end

end
