# Configuration Settings
* global settings
  * $ git config --list
  * $ git config --global user.name "Toshiro Miyamoto"
  * $ git config --global user.email "name@mail.acme.com"
  * $ git config --global color.ui "auto"
* generate an SSH key if you haven't
  * $ ssh-keygen -t rsa -b 4096
  * $ pbcopy < ~/.ssh/id_rsa.pub
* githb.com > Profile > Settings > SSH and GPG keys > New SSH key or Add SSH key
  * Title: My MacBook Pro
  * Key: (paste the key from clipboard)
# Creating a git Project (express)
* initialize git for the project directory
  * $ mkdir express
  * $ cd express
  * $ git init
  * create .gitignore file (.DS_Stores, node_modules, etc.)
  * create README.md
* setup the remote
  * $ git remote -v show
  * $ git remote add origin https://github.com/toshiro-en-miyamoto/express.git
* commit .gitignore and README.md
* push the commit to the remote
  * $ git push -u origin master (OR using IDE such as VScode)
