# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  #home server 
  config.vm.define "homeserver" do |homeserver|
  homeserver.vm.box = 'almalinux/8'
  homeserver.vm.hostname = 'homeserver.example.com'
  homeserver.vm.network "private_network", ip: '192.168.28.2'
  
  homeserver.vm.provision :shell, :inline => "sudo sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config; sudo systemctl restart sshd;"

  end

  #home client 
  config.vm.define "homeclient" do |homeclient|
  homeclient.vm.box = 'almalinux/8'
  homeclient.vm.hostname = 'homeclient.example.com'
  homeclient.vm.network "private_network", ip: '192.168.28.3'
  
  homeclient.vm.provision :shell, :inline => "sudo sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config; sudo systemctl restart sshd;"

  end
end
