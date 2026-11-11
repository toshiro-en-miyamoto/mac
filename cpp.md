# C++ Tooling

## LLVM

> `clang++` of LLVM requires Apple Command Line Tools be installed.

Install LLVM with `brew`. LLD and LLDB are now provided in separate formulae.

```bash
~ % brew install llvm
~ % brew install lld
~ % brew install lldb
```

Set environment variables:

```
export PATH=/opt/homebrew/opt/llvm/bin:$PATH
export LDFLAGS=-L/opt/homebrew/opt/llvm/lib
export CPPFLAGS=-I/opt/homebrew/opt/llvm/include
# export PATH=/opt/homebrew/opt/lldb/bin:$PATH
# export LDFLAGS=-L/opt/homebrew/opt/lldb/lib
# export CPPFLAGS=-I/opt/homebrew/opt/lldb/include
```
