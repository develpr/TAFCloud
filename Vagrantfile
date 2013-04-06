# -*- mode: ruby -*-
# vi: set ft=ruby :
# config.vm.customize ["modifyvm", :id, "--natdnshostresolver1", "on"] solves DNS problems in Ubuntu

Vagrant::Config.run do |config|
        config.vm.box = "magento1702"
        config.ssh.host = "127.0.0.1"
        config.vm.network :forwarded_port, host: 2222, guest: 22
        config.vm.network :forwarded_port, host: 8080, guest: 80
        config.ssh.max_tries = 10
        config.ssh.timeout = 15
        config.vm.customize ["modifyvm", :id, "--memory", 2048]
        config.vm.customize ["modifyvm", :id, "--name", "Magento TAFCloud"]
        config.vm.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
end
