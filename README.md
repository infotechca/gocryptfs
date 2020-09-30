# How to Encrypt Files with gocryptfs on Linux

Do you want to encrypt important files, but not your Linux system’s entire hard drive?<br/>
If so, we recommend gocryptfs encrypts and decrypts everything you store.<br/>
**gocryptfs** Offers Protection from Data Breaches<br/>

## Installing gocryptfs on Debain or Ubuntu like systems.
```bash
sudo apt update
sudo apt install gocryptfs
```
## Installing gocryptfs on Red Hat or Fedora like systems.
```bash
sudo dnf update
sudo dnf install gocryptfs
```
### Creating an Encrypted Directory
```bash
mkdir vault
```
We need to initialize our new directory.<br/>
This step creates the `gocryptfs` file system within the directory:<br/>

```bash
gocryptfs -init vault
```

### Mounting the Encrypted Directory

```bash
mkdir mount
gocryptfs vault mount
```
### let’s Encrypt Some Data
![gocryptfs](https://github.com/infotechca/gocryptfs/blob/master/gocryptfs.gif?raw=true)
---
### Unmounting the Encrypted Directory

```bash
fusermount -u mount
```
