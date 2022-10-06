Vagrant.configure(2) do |config|
    config.vm.box = "generic/ubuntu2004"
    
    config.vm.provider "hyperv" do |h|
        h.enable_virtualization_extensions = true
        h.linked_clone = true
        # h.cpus = 2
        # h.memory = 8192
    end
      
    config.vm.provision "shell", inline: <<-SHELL
    apt-get update -y
    apt-get upgrade -y
    SHELL

    # basic machine 
    config.vm.define "basic" do |b|
        b.vm.hostname = "basic.test"
    end
end