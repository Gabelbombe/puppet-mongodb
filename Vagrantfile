# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant::Config.run do | config |
  config.vm.host_name = 'mongo-module.io'
  config.vm.box       = "hashicorp/precise64"

  #TODO: WILL NOT RUN UNDER CONFIG 2
  config.vm.share_folder "mongodb", "/tmp/vagrant-puppet/modules/mongodb", "."

  config.vm.provision :puppet do | puppet |
    puppet.manifests_path = "tests"
    puppet.manifest_file  = "vagrant.pp"
    puppet.options        = [
      '--modulepath', '/tmp/vagrant-puppet/modules',
      '--verbose'
    ]
  end
end
