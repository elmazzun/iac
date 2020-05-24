# Vagrant options
BOX_NAME = "centos/7"
MACHINES_NUMBER = 2
PROVIDER = "virtualbox"
VM_NAME = "centos-"

# Provider options
PROV_CPUS = 2
PROV_IS_GUI = true
PROV_MEM = 1024

Vagrant.configure("2") do |config|

    # Configure provider
    config.vm.provider PROVIDER do |provider|
        provider.gui = PROV_IS_GUI
        provider.memory = PROV_MEM
        provider.cpus = PROV_CPUS
    end

    # Loop on each VM instance and configure it
    (1..MACHINES_NUMBER).each do |i|
        config.vm.define "#{VM_NAME}#{i}" do |subconfig|
            subconfig.vm.box = BOX_NAME
            subconfig.vm.hostname = "#{VM_NAME}#{i}"
        end
    end

end
