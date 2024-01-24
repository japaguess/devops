Vagrant.configure("2") do |config|


config.vm.provision "shell", path: "script.sh"





  config.vm.define "controle" do |controle|
        controle.vm.box = "shekeriev/debian-11"
        controle.vm.hostname = "controle"
        controle.vm.network "private_network", ip: "172.17.177.100"
        controle.vm.provider "virtualbox" do |vb|
                vb.name = "controle"
                vb.memory = "2048"
                vb.cpus = 2
        end

controle.vm.provision "ansible_local" do |ansible|
            ansible.playbook = "playbook.yml"
            ansible.install_mode = "pip"
        end


# controle.vm.provision "shell", inline: "apt -y install git"	


	end
  config.vm.define "web" do |controle|
        controle.vm.box = "shekeriev/debian-11"
        controle.vm.hostname = "web"
        controle.vm.network "private_network", ip: "172.17.177.101"
        controle.vm.provider "virtualbox" do |vb|
                vb.name = "web"
                vb.memory = "512"
                vb.cpus = 2
        end
	
	end
  config.vm.define "db" do |controle|
        controle.vm.box = "shekeriev/debian-11"
        controle.vm.hostname = "db"
        controle.vm.network "private_network", ip: "172.17.177.102"
        controle.vm.provider "virtualbox" do |vb|
                vb.name = "db"
                vb.memory = "512"
                vb.cpus = 2
        end
	
	end


end