# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Elegimos la imagen que vamos a desplegar, en este caso ubuntu 16.04
  config.vm.box = "ubuntu/trusty64"
  
  # Configuramos el hostname para maquina virtual:
  config.vm.hostname = "vm11"
  config.vm.define "vm11"

  # Asignamos una ip privada a la VM.
  config.vm.network "private_network", ip: "192.168.100.101"

  # Creamos una carpeta compartida
  config.vm.synced_folder "sharedfiles", "/home/vagrant/sharedfiles"

  # Podemos configurar la interaccion con vitualbox, incluyendo las caracteristicas del hardware de la VM
  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    vb.gui = false
    # Podemos personalizar el tamaño de la memoria de la maquina:
    vb.memory = "512"
  end

  # instalamos ansible por comandos de shell
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get install software-properties-common -y
    sudo apt-add-repository ppa:ansible/ansible
    sudo apt-get update
    sudo apt-get install ansible -y
  SHELL
  # Corremos playbook
  config.vm.provision "ansible_local", run: "always" do |ansible|
#    ansible.groups = {
#      'localhost' => ['default']
#    }
    ansible.verbose = "v"
    ansible.limit = 'all,localhost'
    ansible.become = "true"
    ansible.playbook = "installdocker2.yml"
#    ansible.provisioning_path = "/home/vagrant/remoteansible"
  end
end
