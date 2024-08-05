Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"
  
    (1..3).each do |i|
      config.vm.define "server#{i}" do |server|
        server.vm.network "forwarded_port", guest: 80, host: 8080 + i
        server.vm.provider "virtualbox" do |vb|
          vb.memory = "256"
          vb.cpus = 1
        end
      end
    end
  end
  