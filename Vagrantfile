require 'rbconfig'

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

	config.vm.define "rproxy" do |rproxy|
		rproxy.vm.box = "ubuntu/trusty64"
		rproxy.vm.network :forwarded_port, host: 2222, guest: 22, id: 'ssh'
		rproxy.vm.network :forwarded_port, host: 8080, guest: 80
  end

  config.vm.define "app01" do |app01|
		app01.vm.box = "ubuntu/trusty64"
		app01.vm.network :forwarded_port, host: 2223, guest: 22, id: 'ssh'
		app01.vm.network :forwarded_port, host: 8081, guest: 8080
  end

end
