# Configuration Settings
* global settings
  * `$ git config --list`
  * `$ git config --global user.name "Toshiro Miyamoto"`
  * `$ git config --global user.email "name@mail.acme.com"`
  * `$ git config --global color.ui "auto"`
* generate an SSH key if you haven't
  * `$ ssh-keygen -t ed25519 -C "name@mail.acme.com"`
    * depress Enter for the file names
    * depress Enter as a blank passphrase
  * `$ ls -al ~/.ssh`
    * `/.ssh/id_ed25519`
    * `/.ssh/id_ed25519.pub`
  * `touch ~/.ssh/config`, then edit it as follows
    * Host *
      * AddKeysToAgent yes
      * IdentityFile ~/.ssh/id_ed25519
  * Add your SSH private key to the ssh-agent
    * `$ eval "$(ssh-agent -s)"`
    * `$ ssh-add ~/.ssh/id_ed25519`
    * Identity added: /Users/toshiro/.ssh/id_ed25519 (name@mail.acme.com)
  * `$ pbcopy < ~/.ssh/id_ed25519.pub`
* githb.com > Profile > Settings > SSH and GPG keys > New SSH key or Add SSH key
  * Title: My MacBook
  * Key: (paste the key from clipboard)
# Creating a git Project (express)
* initialize git for the project directory
  * `$ mkdir express`
  * `$ cd express`
  * `$ git init`
  * create .gitignore file (.DS_Stores, node_modules, etc.)
  * create README.md
* setup the remote
  * `$ git remote -v show`
  * `$ git remote add origin https://github.com/toshiro-en-miyamoto/express.git`
* commit .gitignore and README.md
* push the commit to the remote
  * `$ git push -u origin master`
  * OR using IDE such as VScode
# Reviewing Your Changes
* checking the status
  * `$ git status`
  * shows changes not staged for commit
  * shows untacked files
* reviewing your changes
  * `$ git diff {<file>}`
  * shows changes in tracked files
* reviewing commit history
  * `$ git log`
  * `$ git log --oneline`
  * shows the commits that youo've made so far with each hash
  * `$ git show <hash>`
  * shows information about the commit identified by a commit hash
  * shows changes in the commit
# Correcting Errors While Working with Git
* undo changes
  * `$ git checkout <file>`
  * reverts the file back to the state during the last commit
* undo git add
  * `$ git restore --staged <file>`
  * unstages the file
* undo git commit
  * `$ git reset --soft HEAD~1`
  * goes back one commit from the last commit
  * `$ git commit --amend -m "New Message"`
  * changes the commit message of the last commit
