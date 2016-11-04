# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.define 'appserver.local' do |c|
    c.vm.box = 'ubuntu/xenial64'
    c.vm.network :private_network, ip: '192.168.9.100'
    c.vm.hostname = 'appserver.local'

    c.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'vagrant.yml'
      ansible.sudo = true
      ansible.inventory_path = 'vagrant-inventory'
      ansible.host_key_checking = false
      ansible.limit = 'all'
      # use any of these: ruby, php, js, elixir
      # ansible.tags = ['ruby']
    end
    # OS X fix @see https://github.com/Varying-Vagrant-Vagrants/VVV/issues/517#issuecomment-122560674
    c.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"
  end
end
