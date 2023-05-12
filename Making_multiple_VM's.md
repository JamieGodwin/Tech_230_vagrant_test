# Making multiple VM's

- We should comment out the npm commands in provision
- Note: If we have 192.168 it will be a local ip address


## Vagrant code 
- The following code is used
``` 
vagrant.configure("2) do |config|
  
  config.vm.define "app" do |app| ### app is defined here
    
    app.vm.box = "ubuntu/bionic64"  ###newer version of linx
    app.vm.network "private_network", ip:"192.168.10.100"

    app.vm.provision "shell", path: "provision.sh"

    app.vm.synced_folder "app", "/home/vagrant/app"
  
  end

  config.vm.define "db" do |db|

    db.vm.box = "ubuntu/bionic64"  ###import linx
    db.vm.network "private_network", ip:"192.168.10.150" ###ip address

    db.vm.synced_folder "environment", "/home/vagrant/environment"

  end

end
```
- Vagrant up can then be done