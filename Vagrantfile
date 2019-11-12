# Install Required Plugins

required_plugins = ["vagrant-hostsupdater"]
required_plugins.each do |plugin|
    exec "vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin
end


#
#
# Vagrant.configure("2") do |config|
#   config.vm.define "app" do |app|
#     app.vm.box = "ubuntu/xenial64"
#     app.vm.network "private_network", ip: "192.168.10.10"
#     app.hostsupdater.aliases = ["app.local"]
#     app.vm.synced_folder "app", "/home/ubuntu/app"
#     app.vm.provision "shell", path: "environment/app/provision.sh", privileged: false
#   end
# end

# -*- mode: ruby -*-
# vi: set ft=ruby :




Vagrant.configure("2") do |config|
  config.vm.define "app" do |app|
    app.vm.box = "ubuntu/xenial64"
    app.vm.network "private_network", ip: "127.0.0.1"
    app.hostsupdater.aliases = ["development.local"]
    app.vm.synced_folder "Python_Uber_Project-master", "/home/ubuntu/Python_Uber_Project_app"
    app.vm.provision "shell", path: "environment/provision.sh", privileged:false 
 end

  # Synced app folder
  # config.vm.synced_folder "Python_Uber_Project-master", "/Python_Uber_Project-master"
#   #
# C:\uber_app_project\vagrant_uber_app\Python_Uber_Project-master


  # provisioning bash script
  # config.vm.provision "shell", path: "environment/provision.sh"
end
