# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.ssh.forward_agent = true
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "development_setup.yml"
    ansible.raw_ssh_args = ["-o UserKnownHostsFile=/dev/null"]
  end
end
