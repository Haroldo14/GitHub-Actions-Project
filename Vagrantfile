# Vagrantfile for two VM

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Global configuration for all machines
  config.vm.box = "ubuntu/jammy64"


  # Worker 1
  config.vm.define "kubeworker1" do |kubeworker1|
  config.vm.synced_folder ".", "/vagrant", owner: "vagrant"
    kubeworker1.vm.hostname = "kubeworker1"
    kubeworker1.vm.network :private_network, ip: "192.168.56.4"
    kubeworker1.vm.provider "virtualbox" do |vb|
      vb.name = "kubeworker1"
      vb.memory = "2048"
      vb.cpus = 2
    end
  end
  # Worker 2
  config.vm.define "kubeworker2" do |kubeworker2|
  config.vm.synced_folder ".", "/vagrant", owner: "vagrant"
    kubeworker2.vm.hostname = "kubeworker2"
    kubeworker2.vm.network :private_network, ip: "192.168.56.5"
    kubeworker2.vm.provider "virtualbox" do |vb|
      vb.name = "kubeworker2"
      vb.memory = "2048"
      vb.cpus = 2
    end
  end
end
