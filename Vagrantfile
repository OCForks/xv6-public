Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/cosmic64"

  config.ssh.forward_agent = true
  config.ssh.forward_x11 = true

  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    # vb.gui = true
    vb.name = "xv6host"
  end

  config.vm.synced_folder ".", "/home/vagrant/xv6", disabled: false

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y build-essential vim emacs-nox nano qemu
  SHELL
end
