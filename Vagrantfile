Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.provision :puppet, :module_path => "private/puppet/modules" do |puppet|
    puppet.manifests_path = "private/puppet/manifests"
    puppet.manifest_file  = "base.pp"
  end

  config.vm.network :forwarded_port, host: 4567, guest: 80

end