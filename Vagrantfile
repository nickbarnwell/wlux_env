Vagrant.configure("2") do |config| 
  config.vm.box = "precise64"

  config.vm.define :wlux_server do |config|
    config.vm.network :forwarded_port, guest: 80, host: 8090
    config.vm.network :private_network, ip: "10.0.5.2"

    config.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "360"]
    end 
  end

  config.vm.define :wlux_test do |config|
    config.vm.network :forwarded_port, guest: 80, host: 8091
    config.vm.network :private_network, ip: "10.0.5.3"

    config.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "128"]
    end 
  end

end
