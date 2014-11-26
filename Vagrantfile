# -*- mode: ruby -*-
# vi: set ft=ruby :

BOX_NAME = ENV["BOX_NAME"] || "trusty"
DOKKU_DOMAIN = ENV["DOKKU_DOMAIN"] || "dokku.me"
DOKKU_IP = ENV["DOKKU_IP"] || "10.0.0.2"

Vagrant::configure("2") do |config|
  config.vm.box = BOX_NAME
  # config.vm.synced_folder File.dirname(__FILE__), "/root/dokku"
  # config.vm.hostname = "#{DOKKU_DOMAIN}"
  config.vm.network :private_network, ip: DOKKU_IP

  # config.vm.provider :virtualbox do |vb|
  #   vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  #   # Ubuntu's Raring 64-bit cloud image is set to a 32-bit Ubuntu OS type by
  #   # default in Virtualbox and thus will not boot. Manually override that.
  #   vb.customize ["modifyvm", :id, "--ostype", "Ubuntu_64"]
  # end
end
