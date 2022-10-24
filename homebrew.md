# Installing Homebrew
- install Apple Command Line Tools (a prerequisit)
- install Homebrew
# Installing Formulae
- `$ brew cask install atom`
- `$ brew cask install webtorrent`
- `$ brew install git`
- `$ brew install node`
  - `$ brew link --force node`
  - `$ brew unlink node`
- installing OpenJDK
  - `$ brew install openjdk`
  - `$ sudo ln -sfn /usr/local/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk`
  - `export JAVA_HOME="$(/usr/libexec/java_home)"` in ~/.zshenv
