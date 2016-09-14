
# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.box = "hashicorp/precise64"
  config.vm.host_name = 'mongo-module.io'
  config.vm.share_folder "mongodb", "/tmp/vagrant-puppet/modules/mongodb", "."

  config.vm.provision :puppet do | puppet |
    puppet.manifests_path = "tests"
    puppet.manifest_file = "vagrant.pp"
    puppet.options = ["--modulepath", "/tmp/vagrant-puppet/modules"]
  end
end
