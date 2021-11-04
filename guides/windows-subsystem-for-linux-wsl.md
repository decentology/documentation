---
description: >-
  Many blockchains will not run on Windows due to platform specific
  applications. However you can utilize WSL in order to match the platform and
  still run natively on Windows
---

# Windows Subsystem for Linux (WSL)

## WSL Setup

Install WSL using the Microsoft store.&#x20;

* You can find the install link here [Microsoft Store (Ubuntu)](https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6?activetab=pivot:overviewtab)
* You can follow the installation steps here: [WSL Install Windows 10](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

**Alternatively **you can follow the steps below to setup a secondary WSL installation

#### Download Image Linux Distribution Image

[https://cloud-images.ubuntu.com/_**groovy**_/current/](https://cloud-images.ubuntu.com/groovy/current/)

### **Import WSL Instance**

```bash
wsl --import <DistributionName> <InstallLocation> <FileName>.wsl.rootfs.tar.gz 
```

### **Launch WSL Instance**

```bash
wsl -d ubuntu2010
```

### Preparing Linux Installation

The following commands will **create a new user **and **set the default shell to bash.** Next you'll set a password for this user account and assign that user the **ability to run sudo commands **for elevated permissions

```bash
useradd -s /bin/bash -m username
passwd username
usermod -aG sudo username
```

Exit WSL instance, terminate and re-login using the non root account

```bash
wsl -t ubuntu2010
wsl -d ubuntu2010 —user username
```

**Install build essentials**. C++ make and build tools. Required for node-gyp building of node.js binaries. Specifically sharp

```bash
sudo apt install build-essential
```

### Installing Software&#x20;

DappStarter utilizes a **node.js **runtime and will need to be pre-installed.

**NVM → NODE → YARN**

### Install Node Version Manager (NVM)

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```

It's often necessary to reset the shell to access new environment variables.

```bash
source ~/.bashrc
```

### **Install Node 14**

```bash
nvm install 14
```

### **Install Yarn**

```bash
npm install -g yarn
```

{% hint style="info" %}
Node 16 has build errors issues with compiling sharp module from source
{% endhint %}

## Remove WSL Instance

```bash
wsl --unregister ubuntu2010
```



