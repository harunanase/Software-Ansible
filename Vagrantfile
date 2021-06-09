# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|

    v.memory = "512"
    v.cpus = 4

    v.default_nic_type = "virtio"
  end

  config.vm.define "target_centos_7" do |target_centos_7|
    target_centos_7.vm.box = "centos/7"

    target_centos_7.vm.network "private_network", ip: "192.168.50.12"
    target_centos_7.vm.network "forwarded_port", guest: 22, host: 2202, host_ip: "127.0.0.1", id: "ssh", auto_correct: true
  end
end
