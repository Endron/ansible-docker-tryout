# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.
  config.vm.define "docker" do |docker|
    docker.vm.box = "ubuntu/trusty64"
    docker.vm.provision "docker"
    docker.vm.provision "ansible" do |ansible|
      ansible.playbook = "bootstrap.yml"
    end
    docker.vm.network "private_network", ip: "192.168.33.10"
  end
end
