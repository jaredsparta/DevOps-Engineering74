# Connect github and localhost with an SSH

* Install gitbash or any terminal
* In your preferred folder run the command 'ssh-keygen -t rsa -b 4096 -C "your_email@example.com"'
* Follow the steps shown to save the key in documents
* Go to your github account -> settings -> SSH and GPG keys
* Click 'New SSH key'
* Navigate to the directory where the .ssh folder was created
* Check with 'ls -a' for private files
* Enter the .ssh file and run 'ls'
* Copy the information in the .pub file
* Paste it in the textbox in 'New SSH key'
