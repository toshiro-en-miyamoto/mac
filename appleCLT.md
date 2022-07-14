# Apple Command Line Tools

`xcode-select` takes 30 minutes to install the Command Line Tools, but it is a quite straight forward way to install and update the tool.

```
% sudo rm -rf /Library/Developer/CommandLineTools
% xcode-select --install
% sudo xcode-select -switch /Library/Developer/CommandLineTools
```
