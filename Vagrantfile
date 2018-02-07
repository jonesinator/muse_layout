Vagrant.configure(2) do |config|
  config.vm.box = "bento/debian-9.3"
  config.vm.network :forwarded_port, guest: 3000, host: 80
  config.vm.network :forwarded_port, guest: 3001, host: 3001
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "provision.yml"
  end
end
