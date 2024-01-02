# Airfoil Common Development Setup

<!-- TOC -->
- [Overview](#overview)
- [Environment](#environment)
- [Software](#software)
- [GitHub](#github)

## Overview

The following instructions need only be done once on a development machine.
*NOTE: These instructions assume that you are running on MacOS*

## Environment

**Ensure the `.bash_profile` is sourced by `zsh`**

```sh
$ cat ~/.zshrc
source ~/.bash_profile
```

If the file doesn't source the `~/.bash_profile` file, then add it with a text editor:

```sh
$ nano ~/.zshrc
```

## Software

**Install JDK 17**

*Download and install the JDK*
https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html

*Retrieve the install path of the JDK*
```sh
$ /usr/libexec/java_home -V
17.0.6 (arm64) "Oracle Corporation" - "Java SE 17.0.6" /Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Hom
```

*Setup the `JAVA_HOME` environment variable*
```sh
$ echo "export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home" >> ~/.bash_profile
$ source ~/.bash_profile
```

## GitHub

**GitHub PAT (Personal Access Token)**

*Create a classic GitHub PAT (Personal Access Token)*
https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-personal-access-token-classic

*Setup the `GPR_USER` and `GPR_KEY` environment variables*
```sh
$ echo "export GPR_USER=<Your_GitHub_Username>" >> ~/.bash_profile
$ echo "export GPR_KEY=<Your_GitHub_Access_Token>" >> ~/.bash_profile
$ source ~/.bash_profile
```
