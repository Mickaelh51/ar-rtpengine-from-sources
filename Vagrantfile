# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "debian/jessie64"
  #config.vm.box = "debian/stretch64"

  # rtpengine
  config.vm.define "rtpengine-dev" do |rtpengine|
    rtpengine.vm.hostname = "rtpengine-dev"
    rtpengine.vm.network :private_network, ip: "10.1.0.225"
    rtpengine.vm.network :private_network, ip: "10.1.1.225"
  end

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", 512]
    vb.customize ["modifyvm", :id, "--cpus", 1]
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "tests/main.yml"
  end

  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.name = "rtpengine-dev"
  end
end
