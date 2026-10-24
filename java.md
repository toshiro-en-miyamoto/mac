## Java on Mac

- Open JDK
- Build tool for Java
  - Maven
- IDE for Java
  - JetBrains IntelliJ IDEA
  - VS Code
  - Eclipse

## OpenJDK

```bash
~% brew install openjdk@25
~% sudo ln -sfn /opt/homebrew/opt/openjdk@25/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-25.jdk

~% /usr/libexec/java_home -V
Matching Java Virtual Machines (1):
    25.0.5.0.2 (arm64) "Homebrew" - "OpenJDK 25.0.5.0.2"
~% java --version
openjdk 25.0.5.0.2 2026-10-22
OpenJDK Runtime Environment Homebrew (build 25.0.5.0.2)
OpenJDK 64-Bit Server VM Homebrew (build 25.0.5.0.2, mixed mode, sharing)

~% brew install openjdk@17
~% sudo ln -sfn /opt/homebrew/opt/openjdk@17/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-17.jdk

~% /usr/libexec/java_home -V
Matching Java Virtual Machines (2):
    25.0.5.0.2 (arm64) "Homebrew" - "OpenJDK 25.0.5.0.2"
    17.0.21.0.2 (arm64) "Homebrew" - "OpenJDK 17.0.21.0.2"
~% java --version
openjdk 25.0.5.0.2 2026-10-22
OpenJDK Runtime Environment Homebrew (build 25.0.5.0.2)
OpenJDK 64-Bit Server VM Homebrew (build 25.0.5.0.2, mixed mode, sharing)
```

Add the following lines in `~/.zshenv`:

```
export JAVA_HOME=$(/usr/libexec/java_home -v 25)
alias jdk25='export JAVA_HOME=$(/usr/libexec/java_home -v 25); java -version'
alias jdk17='export JAVA_HOME=$(/usr/libexec/java_home -v 17); java -version'
```

Then you can flip between versions:

```bash
~% jdk17
openjdk version "17.0.21.0.2" 2026-10-22
OpenJDK Runtime Environment Homebrew (build 17.0.21.0.2+0)
OpenJDK 64-Bit Server VM Homebrew (build 17.0.21.0.2+0, mixed mode, sharing)

~% jdk25
openjdk version "25.0.5.0.2" 2026-10-22
OpenJDK Runtime Environment Homebrew (build 25.0.5.0.2)
OpenJDK 64-Bit Server VM Homebrew (build 25.0.5.0.2, mixed mode, sharing)
```