
VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "couchdb" do |web1|
    web1.vm.box = "ubuntu/bionic64"
    web1.vm.hostname = "couchdb"
    web1.vm.network "private_network", ip: "192.168.30.153"
    web1.vm.synced_folder "~/couchdb", "/var/www/couchdb" ,
        owner: "www-data", group: "www-data",
        mount_options: ["dmode=755","fmode=644"]
    web1.vm.provider :virtualbox do |v|
      v.name = "couchdb"
      v.memory = 512
      v.cpus = 2
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--ioapic", "on"]
    end
  end




end
