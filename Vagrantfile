Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.hostname = "local.jmeter"
  config.vm.network "private_network", ip: "192.168.33.100"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
    ansible.groups = {
      "group1" => ["jmeter"]
    }
  end
end
