# configure 2 VM's

# change to show changes

Vagrant.configure("2") do |config|

  
  config.vm.define "app" do |app| # <- we define app here
    # configures the VM settings
    app.vm.box = "ubuntu/bionic64" #newer version of linx
    app.vm.network "private_network", ip:"192.168.10.100"

    # provision the VM to have Nginx
    app.vm.provision "shell", path: "provision.sh"

    # put the app folder in the VM

    app.vm.synced_folder "app", "/home/vagrant/app"
   end  

   config.vm.define "db" do |db|
    
    db.vm.box = "ubuntu/bionic64" #Import linx 
    db.vm.network "private_network", ip:"192.168.10.150" #ip address, 192.168 gives local ip

    db.vm.synced_folder "environment", "/home/vagrant/environment"
  
   end

end 

