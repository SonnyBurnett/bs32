# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

   config.vm.define :bs32 do |bs32|
      bs32.vm.box = "tsbakker/bs32"  
      bs32.vm.hostname = "bs32"	
	  bs32.vm.network "private_network", type: "dhcp"  
#     bs32.vm.provision :shell, :path => "scripts/bootstrap.sh"
   end
   config.vm.provider "virtualbox" do |v|
      v.gui = false
	  v.memory = 2048
	  v.name = "bs32"
   end
end
