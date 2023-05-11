# How to automate nginx
- In the same folder as the vagrant will be, make a file called provision.sh
- In this file, add the following code:
``` 
#!/bin/bash

sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get install nginx -y
sudo systemctl start nginx
```

- This is the code that will automate nginx in the VM
- Then do: vagrant init
- In the vagrant file, add the code:
``` config.vm.box = "ubuntu/xenial64"
    config.vm.network "private_network", ip: "192.168.10.100"

    config.vm.provision "shell", path: "provision.sh"
```
- Then you can do: vagrant up
- The VM with ingnx should then be made
- You can then ssh into it from git bash 