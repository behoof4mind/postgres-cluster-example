Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.ssh.insert_key = false
  config.vbguest.auto_update = false
  config.vm.synced_folder "./vagrant", "/vagrant", type: "rsync"
  config.vm.provision "ansible_local" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end
end
