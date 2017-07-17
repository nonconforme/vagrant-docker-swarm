# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "box-cutter/ubuntu1604"

  config.vm.define :master do |node|
    node.vm.network :private_network, ip: '192.168.99.10'
  end
  config.vm.define :node1 do |node|
    node.vm.network :private_network, ip: '192.168.99.11'
  end
  config.vm.define :node2 do |node|
    node.vm.network :private_network, ip: '192.168.99.12'
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'docker.yml'
  end
end
