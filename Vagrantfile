# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|

    v.memory = "1024"
    v.cpus = 1

    v.default_nic_type = "virtio"
  end

  config.vm.define "master" do |master|
    master.vm.box = "centos/7"

    master.vm.network "private_network", ip: "192.168.56.11"
    master.vm.network "forwarded_port", guest: 22, host: 22001, host_ip: "127.0.0.1", id: "ssh", auto_correct: true
  end
  config.vm.define "node1" do |node1|
    node1.vm.box = "centos/7"

    node1.vm.network "private_network", ip: "192.168.56.12"
    node1.vm.network "forwarded_port", guest: 22, host: 22002, host_ip: "127.0.0.1", id: "ssh", auto_correct: true
  end
  config.vm.define "node2" do |node2|
    node2.vm.box = "centos/7"

    node2.vm.network "private_network", ip: "192.168.56.13"
    node2.vm.network "forwarded_port", guest: 22, host: 22003, host_ip: "127.0.0.1", id: "ssh", auto_correct: true
  end
end
