# -*- mode: ruby -*-
# vi: set ft=ruby :
# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  if Vagrant.has_plugin?("vagrant-cachier")
	# More info on http://fgrehm.viewdocs.io/vagrant-cachier/usage
	config.cache.scope = :machine
  end

  config.vm.define "wpweekend" do |host1|
    host1.vm.host_name = "wpweekend"
    host1.vm.network "private_network", ip: "10.88.88.10"
    host1.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "512"]
    end
  end
end
