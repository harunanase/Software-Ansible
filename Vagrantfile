# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|

    v.memory = "4096"
    v.cpus = 4

    v.default_nic_type = "virtio"
  end

  config.vm.define "master" do |master|
    master.vm.box = "centos/7"

    master.vm.network "private_network", ip: "192.168.50.11"
    master.vm.network "forwarded_port", guest: 22, host: 22001, host_ip: "127.0.0.1", id: "ssh", auto_correct: true
  end
  config.vm.define "node2" do |node2|
    node2.vm.box = "centos/7"

    node2.vm.network "private_network", ip: "192.168.50.12"
    node2.vm.network "forwarded_port", guest: 22, host: 22002, host_ip: "127.0.0.1", id: "ssh", auto_correct: true
  end
  config.vm.define "node3" do |node3|
    node3.vm.box = "centos/7"

    node3.vm.network "private_network", ip: "192.168.50.13"
    node3.vm.network "forwarded_port", guest: 22, host: 22003, host_ip: "127.0.0.1", id: "ssh", auto_correct: true
  end
end
