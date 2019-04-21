Vagrant.configure("2") do |config|
  # config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant"
  config.vm.box = "generic/debian9"

  config.vm.define "node1" do |machine|
    # machine.vm.box = "generic/debian9"
    machine.vm.network "private_network", ip: "172.17.177.21"
  end

  config.vm.define "node2" do |machine|
    # machine.vm.box = "generic/debian9"
    machine.vm.network "private_network", ip: "172.17.177.22"
  end
  
  config.vm.define "node3" do |machine|
    # machine.vm.box = "generic/debian9"
    machine.vm.network "private_network", ip: "172.17.177.23"
  end

  config.vm.define 'controller' do |machine|
    machine.vm.network "private_network", ip: "172.17.177.11"

    machine.vm.provision :ansible_local do |ansible|
      ansible.playbook       = "playbook.yml"
        ansible.host_vars = {
          "node1" => {"TESTVAR" => 111,
                      "maxRequestsPerChild" => 808},
          "node2" => {"TESTVAR" => 222,
                      "maxRequestsPerChild" => 909},
          "node3" => {"TESTVAR" => 333,
                      "maxRequestsPerChild" => 909}
        }
      ansible.verbose        = true
      ansible.install        = true
      ansible.limit          = "all" # or only "nodes" group, etc.
      ansible.inventory_path = "inventory"
    end
  end

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
