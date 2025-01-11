Vagrant.configure("2") do |config|
	config.vm.define "web_server" do |web|
	config.vm.box = "ubuntu/bionic64"
	web.vm.hostname = "web-server"
	
web.vm.provider "virtualbox" do |vb|
	vb.memory = "2048"
	vb.cpus = 2
	end

web.vm.network "private_network", ip: "192.168.33.10"

web.vm.synced_folder "./app", "/app"

web.vm.provision "shell", inline: <<-shell
	sudo apt-get update
	sudo apt-get install -y apache2
shell
	
 end
 end
 