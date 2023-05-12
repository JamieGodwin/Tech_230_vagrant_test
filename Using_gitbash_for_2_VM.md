# Using two terminals for the two VM's (db terminal)

## db terminal
- we must first cd into the right place: ``` cd OneDrive/Desktop/Tech_230/app/Tech_230_multi_machine ```
- We can then ssh in with: ``` vagrant ssh db ```
- We then do the standard code: ``` sudo apt-get update -y , sudo apt-get upgrade -y ```
## We are now adding mongodb
- Then add the code: ``` sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv D68FA50FEA312927 ```
- Then the code: ``` echo "deb https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list ```
Then add: ``` sudo apt-get update -y , sudo apt-get upgrade -y ```
Then add ``` sudo apt-get install -y mongodb-org=3.2.20 mongodb-org-server=3.2.20 mongodb-org-shell=3.2.20 mongodb-org-mongos=3.2.20 mongodb-org-tools=3.2.20 ```
Then add: ``` sudo systemctl start mongod ```
Then add: ``` sudo systemctl enable mongod ```
Then add: ``` sudo systemctl status mongod ``` to check the status

## Need to check what these commands are for still!
Then add: ``` sudo nano /etc ```
Then add: ``` sudo nano /etc/mongod.conf ```
Then add: ``` sudo systemctl restart mongod ```
Then add: ``` sudo systemctl enable mongod ```