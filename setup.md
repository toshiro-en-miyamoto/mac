# Setting up Mac

- install Apple Command Line Tools (a prerequisite)
- install Homebrew
- setup `git`

## Apple Command Line Tools

```bash
~$ sudo rm -rf /Library/Developer/CommandLineTools
~$ xcode-select --install
~$ sudo xcode-select --switch /Library/Developer/CommandLineTools
```

## Homebrew

```bash
~$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## `git`

`git` comes with Apple Command Line Tools.
You just need `pbcopy` to copy/paste.

```bash
~$ brew install pbcopy
```

### Setup `git`

#### Global settings:

```bash
~$ git config --list
~$ git config --global user.name "your name"
~$ git config --global user.email "yours@mail.acme.com"
~$ git config --global color.ui "auto"
```

#### SSH key:

```bash
~$ ssh-keygen -t ed25519 -C "yours@mail.acme.com"
```

- depress Enter for the file names
- depress Enter as a blank passphrase

Then, you get the following files:

```bash
~$ ls -al ~/.ssh
/.ssh/id_ed25519
/.ssh/id_ed25519.pub
```

#### SSH configuration:

Create the configuration file `touch ~/.ssh/config`, then edit it as follows:

```bash
Host github.com
  AddKeysToAgent yes
  IdentityFile ~/.ssh/id_ed25519
```

Add your SSH private key to the SSH agent:

```bash
~$ eval "$(ssh-agent -s)"
~$ ssh-add ~/.ssh/id_ed25519
```

#### SSH key to `github`

```bash
  * `$ pbcopy < ~/.ssh/id_ed25519.pub`
```

`github.com` > Profile > Settings > SSH and GPG keys > New SSH key or Add SSH key:

- Title: (any title you want)
- Key: (paste the key from clipboard)
