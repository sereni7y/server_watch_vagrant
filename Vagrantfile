# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
	
	config.vm.define 'webserver' do |ws|
		ws.vm.box = 'bento/centos-7.2'
		ws.vm.hostname = 'webserver-001'
		ws.vm.network 'private_network', ip: '10.1.1.33'
		ws.vm.network 'forwarded_port', guest: 80, host: 8080
		
		ws.vm.provider 'virtualbox' do |v|
			v.memory = 2048
			v.cpus = 2
		end
	end
	
	config.vm.define 'server-001' do |s1|
		s1.vm.box = 'bento/centos-7.2'
		s1.vm.hostname = 'server-001'
		s1.vm.network 'private_network', ip: '10.1.1.34'
	end
  
	config.vm.define 'server-002' do |s2|
		s2.vm.box = 'bento/centos-7.2'
		s2.vm.hostname = 'server-002'
		s2.vm.network 'private_network', ip: '10.1.1.35'
	end
end
