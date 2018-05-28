# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "generic/rhel7" 
  config.vm.synced_folder '.', '/vagrant'  
  #config.vm.network "private_network", ip: "10.0.2.15"
  #config.vm.provision :shell, path: "bootstrap.sh"
  #config.vm.network :forwarded_port, guest: 80, host: 4567
  config.vm.provision "ansible_local" do |ansible|
	ansible.playbook = "playbook.yml"
	ansible.install_mode = "pip"
	ansible.version = "2.5.0"
	#ansible.pip_args = "-r /vagrant/requirements.txt"
	ansible.inventory_path = 'hosts'
	ansible.verbose = true
    ansible.install = true
	ansible.limit = 'all'
	#ansible.gather_facts = true
  end

  # config.vm.box_check_update = false
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
