Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder "./vagrant", "/vagrant", type: "virtualbox"
  config.vm.box = "generic/debian9"

  config.vm.define "node1" do |machine|
    machine.vm.box = "generic/debian9"
    machine.vm.network "private_network", ip: "192.168.50.10"
  end
  #   config.vm.define "node2" do |machine|
  #   machine.vm.box = "generic/debian9"
  #   machine.vm.network "private_network", ip: "192.168.50.11"
  # end

  config.vm.define 'controller' do |machine|
    machine.vm.network "private_network", ip: "192.168.50.9"

    machine.vm.provision :ansible_local do |ansible|
      ansible.playbook       = "playbook.yml"
      ansible.verbose        = true
      ansible.install        = true
      ansible.limit          = "all" # or only "nodes" group, etc.
      ansible.inventory_path = "vagrant.py"
    end
  end


  # config.vm.define "node2" do |node2|
  #   node2.vm.box = "generic/debian9"
  #   config.vm.network "private_network", ip: "192.168.50.5"
  # end
  # config.vm.define "node3" do |node2|
  #   node2.vm.box = "generic/debian9"
  #   config.vm.network "private_network", ip: "192.168.50.6"
  # end


  # config.ssh.insert_key = false
  # config.vm.provision "ansible_local" do |ansible|
  #   ansible.verbose = "v"
  #   ansible.playbook = "playbook.yml"
  #   ansible.extra_vars = {
  #     ntp_server: "pool.ntp.org",
  #     node1: {
  #       ip: 192.168.50.4,
  #       workers: 4
  #     },
  #     node2: {
  #       ip: 192.168.50.5,
  #       workers: 4
  #     },
  #     node3: {
  #       ip: 192.168.50.6,
  #       workers: 4
  #     },
  #   }
  # end
end
