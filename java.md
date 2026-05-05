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
~$ brew install openjdk
~$ sudo ln -sfn /usr/local/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk`
```

Add the following line in `~/.zshenv`:

```
export JAVA_HOME="$(/usr/libexec/java_home)"
```
