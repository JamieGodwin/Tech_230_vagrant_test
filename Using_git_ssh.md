#  Making public and private keys
- The private key is the secure one, and it "unlocks" the public key
- First do: ` ls -a `
- We should see ` .ssh/ ` file
- Do ` cd .ssh `
- Then ` ssh-keygen -t rsa 4096 -C "jamieglfc@gmail.com"
- You don't need a passphrase if you don't want one
- If you ` ls ` you should have the name of your key and the name.pub
- To find the key info, do: ` cat Jamie_ssh_github_test.pub `
- Note: The name above is what I chose to set it as when maing the key.
## Working on github
- On github, we can make a new ssh key by finding the option in settings.
- When making the key, under the "key" heading we add the key info we got from the terminal.
## Back to terminal
- We then need to add: `ssh-agent -s`  with backticks around the whole thing.
- Then: ` ssh-add ~/.ssh/Jamie_ssh_github_test ` 
- We can then check with ` ssh -T git@github.com `

## Adding to github
- We then cd into the folder we want in the regular way
- ` git init `
- ` git add . `
- ` git commit -m "name" `
- ` git push -u origin main `
- Note: on mine, it works with "master" rather than main