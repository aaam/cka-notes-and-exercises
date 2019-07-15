# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.define "kube-master1" do |master|
    master.vm.box = "bento/ubuntu-16.04"
    master.vm.hostname = "kube-master1"
    master.vm.network "public_network", bridge: "enp7s0"
    master.vm.provider "virtualbox" do |v|
      v.cpus = "2"
      v.memory = "2048"
    end
  end

  (1..2).each do |i|
    config.vm.define "worker-#{i}" do |worker|
      worker.vm.box = "bento/ubuntu-16.04"
      worker.vm.hostname = "worker-#{i}"
      worker.vm.network "public_network", bridge: "enp7s0"
      worker.vm.provider "virtualbox" do |v|
        v.cpus = "2"
        v.memory = "2048"
      end
    end
  end
end
