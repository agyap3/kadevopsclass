# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.provision "shell", inline: "echo Welcome to Linux Lab Server"
  config.vm.define "server1" do |server1|
  config.vm.box = 'almalinux/8'
  config.vm.network "private_network", ip: '192.168.28.2'
  config.vm.hostname = 'server1.example.com'
  #config.ssh.port = '2200'
  config.ssh.forward_agent = true
  config.vm.provider "virtualbox" do |vb|
    vb.name = 'homeserver'
    vb.cpus = '2'
    vb.memory = '1024'
  config.vm.provision "shell", inline: <<-SHELL
    dnf update -y
  SHELL
  end
end

  config.vm.provision "shell", inline: "echo Welcome to Linux Student Desktop2"
  config.vm.define "desktop2" do |desktop2|
  config.vm.box = 'almalinux/8'
  config.vm.network "private_network", ip: '192.168.28.3'
  config.vm.hostname = 'desktop2.example.com'
  #config.ssh.port = '2201'
  config.ssh.forward_agent = true
  config.vm.provider "virtualbox" do |vb|
    vb.name = 'homeclient'
    vb.cpus = '2'
    vb.memory = '1024'
  config.vm.provision "shell", inline: <<-SHELL
    dnf update -y
  SHELL
  end
end
end