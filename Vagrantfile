# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  #config.vm.box = "ubuntu/xenial64"
  config.vm.box = "cbednarski/ubuntu-1604"

  config.vm.hostname = "withknown"
  config.vm.network :private_network, ip: "192.168.33.33"

  config.vm.synced_folder "./Known", "/home/vagrant/Known", :group => "www-data", :mount_options => ['dmode=775','fmode=664']

  # Ansible provisioner.
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/develop.yml"
    ansible.sudo = true
  end

end
