# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "ubuntu64"

  config.vm.host_name = 'rails-dev-box'
  config.vm.forward_port 3000, 3000
  config.vm.forward_port 9292, 9292
  config.vm.forward_port 80, 8080


  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = "cookbooks"
    # chef.recipe_url = "http://files.vagrantup.com/getting_started/cookbooks.tar.gz"
    # chef.add_recipe("vagrant_main")

    chef.add_recipe "apt"
    # chef.add_recipe "omnibus-updater"
    chef.add_recipe "vim"
    chef.add_recipe "sqlite"
    chef.add_recipe "passenger_apache2"
    chef.add_recipe "nodejs"
    # chef.add_recipe "apache2"
  #  chef.add_recipe "rvm"
  #  chef.add_recipe "rvm::system"
  #  chef.add_recipe "chef_handler"
  #  chef.add_recipe "minitest-handler"
  #  chef.add_recipe "arangodb::install_deb"

 end

end
