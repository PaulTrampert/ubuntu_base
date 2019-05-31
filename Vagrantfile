Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.provision "shell", run: "always", inline: "sudo rm -rf /usr/share/ansible/roles/ubuntu_base || true && sudo mkdir -p /usr/share/ansible/roles && sudo cp -r /vagrant /usr/share/ansible/roles/ubuntu_base"

  config.vm.provision "ansible_local", run: "always" do |ansible|
    ansible.playbook = "tests/test.yml"
  end
end
