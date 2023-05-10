# How to open linux
- open git bash
- find the directory that the file you want to open is
- cd into each part (cd onedrive, cd desktop, cd virtual, ...)
- vagrant ssh

# commands in linux/bash
- touch example.txt makes a txt file with name "example"
- ls lets you know the contents
- Note: linux is case sensitive
- you can read a file with: fiel example.txt
- cat example.txt allows you to read the file
- sudo nano example.txt allows you to add writing to the file.
Note: Once finished writing, ctrl x
- mkdir "name" creates a directory
- rm example.txt will remove the text file
- rm -rf "name" will remove the directory
- To make a hidden directory: mkdir ."name"
- To view the hidden files, ls -a
- ls *my allows you to find directories with "my" in them 
- ls my* allows you to find files with "my" in them 
- ls -l allows you to see access to files for users (w,r,x = write, read and execute)
- chmod u+x example.txt allows for owner to execute the file.
- sudo chmod 777 example.txt allows for everyone to do everything