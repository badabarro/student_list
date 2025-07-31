Vagrant.configure("2") do |config|
  config.vm.define "docker" do |docker|
    docker.vm.box = "eazytrainingfr/centos7"
    docker.vm.box_version = "1.0"
    #docker.vm.network "private_network", type: "dhcp"
    docker.vm.network "private_network", type: "static", ip: "192.168.56.5"
    docker.vm.hostname = "docker"
    docker.vm.provider "virtualbox" do |v|
      v.name = "docker"
      v.memory = 1024
      v.cpus = 2
    end
    docker.vm.provision :shell do |shell|
      shell.path = "install_docker.sh"
      shell.env = { 'ENABLE_ZSH' => ENV['ENABLE_ZSH'] }
    end
  end
end