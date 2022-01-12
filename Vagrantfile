Vagrant.configure("2") do |config|
    #box vm
    config.vm.box = "ubuntu/bionic64"
    #link da vm (problema de ssl)
    config.vm.box_download_insecure = " https://vagrantcloud.com/ubuntu/boxes/bionic64/versions/20211216.0.0/providers/virtualbox.box"
    #config de hardware do HyperVisor
    config.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
    end
  
  
    config.vm.define "docker" do |docker|
  
  
      #liberar ip rede pública para acesso da rede interna
      docker.vm.network "public_network", ip: "192.168.101.31"
      #config de hardware do HyperVisor
      config.vm.provider "virtualbox" do |vb|
        vb.memory = 3000
        vb.cpus = 2
        vb.name = "docker_machine"
      end
    end
  end
  