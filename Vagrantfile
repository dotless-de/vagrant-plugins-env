# -*- mode: ruby -*-
# vi: set ft=ruby :

# we need to manually require the plugin, since it was not
# installed using `vagrant plugin install`.
# Guard the call to be backward compatible to vagrant 1.0
Vagrant.require_plugin 'vagrant-vbguest' if Vagrant.respond_to?(:require_plugin)

# class My_Installer < VagrantVbguest::Installers::Linux
#   def self.match?(vm)
#     VagrantVbguest::Installers::Linux.match? vm
#   end
#
#   def install(opts=nil, &block)
#     vm.ui.success "Running my own installer!"
#     super
#   end
#
#   def running?(opts=nil, &block)
#     vm.ui.success "Testing my own installer!"
#     super
#   end
# end
# VagrantVbguest::Installer.register My_Installer, 10

# Old style (vagrant 1.0) config block
Vagrant::Config.run do |config|
  config.vm.box = "lucid32"
  config.vm.box_url = "http://files.vagrantup.com/lucid32.box"
  config.vm.network :hostonly, "33.33.33.200"
  config.vm.host_name = "vagrant-1.1-box"


  # config.vbguest.auto_update = false
  # config.vbguest.iso_path = '/Applications/VirtualBox.app/Contents/MacOS/VBoxGuestAdditions.iso'
  # config.vbguest.iso_path = 'http://download.virtualbox.org/virtualbox/%{version}/VBoxGuestAdditions_%{version}.iso'


  # set auto_update to false, if do NOT want to check the correct additions
  # version when booting this machine
  config.vbguest.auto_update = false

  # set this to let the check run each time, but don't install anything
  # config.vbguest.no_install = true

  # do NOT download the iso file from a webserver
  #config.vbguest.no_remote = true

  # config.vbguest.installer = My_Installer
end
