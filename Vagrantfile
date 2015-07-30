Vagrant.configure("2") do |config|
  config.vm.box      = "debian73"
  config.vm.box_url  = "http://puppet-vagrant-boxes.puppetlabs.com/debian-73-x64-virtualbox-nocm.box"

  config.vm.network :forwarded_port, guest: 8080, host: 8888, auto_correct: true

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", 2048]
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provisioning/playbook.yml"

    ansible.host_key_checking = false
  end
end
