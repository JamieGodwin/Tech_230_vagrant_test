# How to add an app/file contents to the VM

- Firstly, the app file needs to be unzipped 
- The app contents then needs to be moved into virtual studio
- We can then do the command: vagrant init
- The following additional code is then added:
``` 
config.vm.synced_folder "app", "/home/vagrant/app"

```
- Here the "app" refers to the folder you want to sync from your computer
- /home/vagrant is where in the VM you want the app to appear.
- The second "app" is what's being synced to the VM.  
- You can then do the command: vagrant up

# Working in git bash
- You then put into git bash the command: vagrant ssh 
- You then cd into the app folder. May have to find it by using pwd.
- The different requirements can then be loaded into the VM

## Downloading nodejs
- You can do the command sudo apt-get install nodejs -y

## Getting the right version of nodejs (in git bash)
- First do the command: sudo apt-get install python-software-properties
- Then the command: curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
- Then the code: sudo apt-get install nodejs -y

## Installing npm
- Do the code: npm install
- Do the code: nom start
- Should recieve the message of the port number
- To view the port, do "ip address:port number"
!["final image"](image (6).png)