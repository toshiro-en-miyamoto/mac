# Apple Command Line Tools

`xcode-select --install` takes 30 minutes to install the Command Line Tools, but it is a quite straight forward way to install and update the tool.

```bash
% sudo rm -rf /Library/Developer/CommandLineTools
% xcode-select --install
% sudo xcode-select --switch /Library/Developer/CommandLineTools
```
