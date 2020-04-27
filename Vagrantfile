# -*- mode: ruby -*-
# bump your IPs and include version when adding new boxes
# https://app.vagrantup.com/debian

  role = File.basename(File.expand_path(File.dirname(__FILE__)))
  gui = true
  ENV['VAGRANT_DEFAULT_PROVIDER'] = ''

  boxes = [
  

  ]

  Vagrant.configure("2") do |config|
    boxes.each do |box|

      

      config.vm.define box[:name] do |vms|
        vms.vm.box = box[:box]
        vms.disksize.size = box[:disk_size]
        vms.vm.box_version = box[:version]
        vms.vm.guest = box[:distribution]
        vms.vm.hostname = box[:name]
        # vms.vm.synced_folder ".vagrant/synced", "/home/vagrant"

        

        vms.vm.network :private_network, ip: box[:ip]

        vms.vm.provision "shell",
          inline: "echo 'up and running'"

        vms.vm.provision "vai" do |ansible|
          ansible.inventory_dir='tests/vagrant'
          ansible.inventory_filename='generated_inventory'
          ansible.groups = {
          
          }
        end

        vms.vm.provision "shell",
          inline: "echo 'system booted'"

        vms.vm.provision :ansible do |ansible|
          ansible.playbook = "tests/vagrant/site.yml"
          ansible.verbose = "vv"
        end
      end
    end
  end
end

# vi: set ft=ruby ts=2 sw=2 tw=0 et :