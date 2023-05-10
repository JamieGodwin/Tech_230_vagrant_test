## vagrant init
## config.vm.box = "ubuntu/xenial64"
## config.vm.network "private_network", ip:"192.168.10.100"
add the above two into vagrant
## vagrant up
## vagrant ssh 
## sudo apt-get update
## sudo apt-get upgrade
## sudo apt-get install nginx -y
## sudo systemctl start nginx
## sudo systemctl status nginx
## ctrl+c to get terminal back

# If you want to add an ip address, do:
exit
add ip address
vagrant reload 

# should now be working


## terminal it bash.
find where you are cd into where you are after the users name part.
Use pwd to find the file path. Then cd into the right place. Then do vagrant ssh.