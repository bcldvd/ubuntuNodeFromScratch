#Set up a NodeJS Server on Ubuntu from scratch

## Table of Contents

* [Prerequisite](#Prerequisite)
* [SSH](#ssh)
* [FTP](#ftp)


## Prerequisite

Take control of the  `root` user

```
sudo passwd
```

## SSH

Install Open-SSH in order to ssh on your server and work from your current machine's terminal if the ubuntu server is on a virtual machine (Allowing you to have the correct keyboard layout and do copy and paste actions in the terminal)

```
apt-get install openssh-client
apt-get install openssh-server
```

## FTP

Install an FTP server in order to send files to your server easily (such as NodeJS :) )

```
sudo apt-get install vsftpd
nano /etc/vsftpd.conf
```

Modify this configuration files accordingly :

```
anonymous_enable=YES
write_enable=YES
```

Save it (`Ctrl+X` with nano) and restart the server

```
service vsftpd restart
```

## Node

```
sudo apt-get install g++
cd ~/workspace
git clone https://github.com/joyent/node.git && cd node
git checkout v0.10.26
mkdir ~/opt && mkdir ~/opt/node
./configure --prefix=~/opt/node
make
make install
```

