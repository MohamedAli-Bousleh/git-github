# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # jenkinsserver
  config.vm.define "Debian" do |docker|
    docker.vm.box = "debian/buster64"
    docker.vm.hostname = "MyDebian"
    docker.vm.box_url = "debian/buster64"
    docker.vm.network :private_network, ip: "192.168.10.10"
	docker.vm.disk :disk, name: "backup", size: "50GB"
    docker.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
      v.customize ["modifyvm", :id, "--memory", 8072]
      v.customize ["modifyvm", :id, "--name", "MyDebian"]
      v.customize ["modifyvm", :id, "--cpus", "3"]
    end
  end
end


