The following is used in the nginx provision file.
` #!/bin/bash `

` sudo apt-get update -y `

` sudo apt-get upgrade -y `

` sudo apt-get install nginx -y `

` sudo systemctl start nginx `

` sudo apt-get install nodejs -y `

` sudo apt-get install python-software-properties `

` curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash - `

` sudo apt-get install nodejs -y `

` sudo npm install pm2 -g `

` cd /home/vagrant/app `
 

` # npm install `

` # npm start `