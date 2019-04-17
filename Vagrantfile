Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder "./vagrant", "/vagrant", type: "rsync"

  config.vm.define "node1" do |node1|
    node1.vm.box = "generic/debian9"
  end

  config.vm.define "node2" do |node2|
    node2.vm.box = "generic/debian9"
  end
  config.vm.define "node3" do |node3|
    node3.vm.box = "generic/debian9"
  end

  config.ssh.insert_key = false
#  config.vbguest.auto_update = false
  config.vm.synced_folder "./vagrant", "/vagrant", type: "rsync"
  config.vm.provision "ansible_local" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end
end
