Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8090
  #config.vm.network "public_network" <-- Dessa forma pega do DHCP
  config.vm.network "public_network", ip: "192.168.0.200"
  #config.vm.provision "shell",
  #  inline: "apt update && apt -y install nginx && service nginx start"
  config.vm.provision "shell", path: "provision.sh"
end
