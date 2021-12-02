
Vagrant.configure("2") do |config|

  config.vm.define "vm1" do |vm1|
    vm1.vm.box = "centos/7"
    vm1.vm.hostname = "machine1"

    vm1.vm.provider :virtualbox do |v|
      v.memory = 512
      v.cpus = 2
    end
  end

  config.vm.define "vm2" do |vm2|
    vm2.vm.box = "ubuntu/trusty64"
    vm2.vm.hostname = "machine2"
    vm2.vm.network "forwarded_port", guest: 80, host: 8081, host_ip:"127.0.0.1"

    vm2.vm.provider :virtualbox do |v|
      v.memory = 512
      v.cpus = 2
    end
  end
end