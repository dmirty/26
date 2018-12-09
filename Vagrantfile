# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
  config.vm.synced_folder ".", "/vagrant",type:"virtualbox"
  config.vm.provider "virtualbox" do |v|
      v.memory = 1024
      v.cpus = 1
  end
  

  config.vm.define "dmug.local" do |dmug.local|
    dmug.local.vm.network "public_network", ip: "192.168.1.60"
    dmug.local.vm.hostname = "dmug.local"
	dmug.local.vm.provision "shell", inline: <<-SHELL
          mkdir -p ~root/.ssh
                cp ~vagrant/.ssh/auth* ~root/.ssh
        SHELL
  end

 
 


end
