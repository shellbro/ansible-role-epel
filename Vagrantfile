Vagrant.configure("2") do |config|
  config.vbguest.auto_update = false
  
  config.vm.define "centos" do |centos|
    centos.vm.box = "centos/7"
    centos.vm.provision "ansible" do |a|
      a.limit = "all"
      a.playbook = "tests/test-vagrant.yml"
    end
  end
end
