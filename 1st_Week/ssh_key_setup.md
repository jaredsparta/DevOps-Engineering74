# Connect github and localhost with an SSH key

* Install gitbash or any terminal
* In your preferred folder run the command 
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
* Follow the steps shown to save the key in documents
* Go to your GitHub account -> settings -> SSH and GPG keys
* Click 'New SSH key'
* Navigate to the directory where the .ssh folder was created
* Check with the following for private files (ones that start with .)
```
ls -a
```
* Enter the .ssh directory and run 'ls'
* Copy the information in the .pub file (the public key info)
* Paste it in the textbox in GitHub 'New SSH key'

-----------------------------------------------------------
* Key commands to add files to be committed:
```
git add . 
git commit -m 'message for commit'
git push
```
