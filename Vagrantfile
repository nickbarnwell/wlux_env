Vagrant.configure("2") do |config| 
  config.berkshelf.enabled = true
  config.vm.box = "precise64"


  config.vm.define :wlux_server do |config|
    config.vm.hostname = "wlux"
    config.vm.network :forwarded_port, guest: 80, host: 8090

    config.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "360"]
    end 

  end
  
  config.vm.synced_folder "weblabux/", "/opt/lampp/htdocs/weblabux"

  config.vm.provision :shell, :inline => "mkdir -p /var/chef/cache"
  config.vm.provision "chef_solo" do |chef|
    chef.cookbooks_path = ["cookbooks", "./cookbooks"]
    chef.add_recipe "apt"
    chef.add_recipe "xampp"
    chef.add_recipe "git"
    chef.add_recipe "wlux_dev::default"
  end
end
