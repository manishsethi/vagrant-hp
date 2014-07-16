# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!


VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "base"
  config.vm.provider :hp do |rs|
    rs.access_key  = ENV['HP_ACCESS_KEY']
    rs.secret_key = ENV['HP_SECRET_KEY']
    rs.flavor   = "standard.xsmall"
    rs.tenant_id = ENV['HP_TENANT_ID']
    rs.server_name = "vagrant-server"
    rs.image    = "75d47d10-fef8-473b-9dd1-fe2f7649cb41"
    rs.keypair_name = "manish-hp"
    rs.ssh_private_key_path = "/home/ubuntu/.ssh/id_rsa"
    rs.ssh_username = "ubuntu"
    rs.availability_zone = "us-east"
    # Security Groups defaults to ["default"]
    # rs.security_groups = ["group1", "group2"]
    # rs.floating_ip ="33.33.33.10" # Optional
    # rs.network = ["830744ee-38a8-4618-a1eb-7c06fcsdf78", "Test_Network"] # Optional
  end
end
