# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "openguide"
  config.vm.box_check_update = true
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.host_name = "openguide.dev"
  config.vm.synced_folder "www", "/var/www", :mount_options => ["dmode=777", "fmode=666"]

end
