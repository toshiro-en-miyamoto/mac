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
export LLVM="$(brew --prefix llvm)"
export PATH=${LLVM}/bin:$PATH
export LDFLAGS="-L${LLVM}/lib/c++ -L${LLVM}/lib/unwind -lunwind -Wl,-rpath,${LLVM}/lib/c++"
export CPPFLAGS=-I${LLVM}/include
export LLDB="$(brew --prefix lldb)"
export PATH=${LLDB}/bin:$PATH
```

### Using LLVM with Visual Studio Code

For the best experience with upstream LLVM, use the official LLVM language server (`clangd`) for code completion and linting, paired with a debugger extension.

- Install `clangd`. Search for and install the official `clangd` extension (`llvm-vs-code-extensions.vscode-clangd`).
- Avoid IntelliSense conflicts. If you also have Microsoft's C/C++ extension installed, disable its IntelliSense engine by setting "C_Cpp.intelliSenseEngine": "disabled" in your VS Code settings.
- Install a debugger. Search for and install the official `lldb` extension (`llvm-vs-code-extensions.lldb-dap`).
