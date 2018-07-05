Vagrant.configure("2") do |config|
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.box = "centos/7"
  config.vm.network 'private_network', ip: '192.168.56.10'
  config.vm.provision :ansible_local do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.inventory_path = 'inventory'
	ansible.limit = 'all'
  end
end