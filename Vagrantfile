# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  #home server configs
  config.vm.define "homeserver" do |homeserver|
  config.vm.box = 'almalinux/8'
  config.vm.network "private_network", ip: '192.168.28.2'
  config.vm.hostname = 'homeserver.example.com'
  #config.ssh.port = '2200'
  config.ssh.forward_agent = true
  config.vm.provider "virtualbox" do |vb|
   # vb.name = 'homeserver1'
    vb.cpus = '1'
    vb.memory = '1024'
    vb.gui = true
  #config.vm.provision "shell", inline: <<-SHELL
   # "echo Welcome to home Linux Lab Server" 
    #dnf update -y
  #SHELL
   end
  end

  #home client configs
  config.vm.define "homeclient" do |homeclient|
  config.vm.box = 'almalinux/8'
  config.vm.network "private_network", ip: '192.168.28.3'
  config.vm.hostname = 'homeclient.example.com'
  #config.ssh.port = '2201'
  config.ssh.forward_agent = true
  config.vm.provider "virtualbox" do |vb|
    #vb.name = 'homeclient1'
    vb.cpus = '1'
    vb.memory = '1024'
    vb.gui = true
  #config.vm.provision "shell", inline: <<-SHELL
   # "echo Welcome to Linux homeclient Lab Server"
    #dnf update -y
  #SHELL
  end
  end
end
