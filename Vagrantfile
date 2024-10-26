# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/lunar64"
  config.vm.box_url = "file:///vms/package.box"
  config.vm.box_check_update = false
  config.vm.network "forwarded_port", guest: 80, host: 80
  config.vm.network "forwarded_port", guest: 443, host: 443
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.synced_folder ".", "/opt/myapp"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "ubuntu1"
    vb.memory = "2048"
  end
end
