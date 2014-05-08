#Set up a NodeJS Server on Ubuntu from scratch

## Table of Contents

* [Prerequisite](#Prerequisite)
* [SSH](#ssh)
* [FTP](#ftp)


## Prerequisite

Take control of the  `root` user & create a workspace folder

```
sudo passwd
mkdir ~/workspace
sudo ln -s ~/workspace/ /workspace
```

## SSH

Install Open-SSH in order to ssh on your server and work from your current machine's terminal if the ubuntu server is on a virtual machine (Allowing you to have the correct keyboard layout and do copy and paste actions in the terminal)

```
sudo apt-get install openssh-client
sudo apt-get install openssh-server
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
sudo service vsftpd restart
```

## GIT

### Installation

```
sudo apt-get install git
```

### Configuration

```
nano ~/.gitconfig
```

Add your infos accordingly, example with my infos : 

```
[color]
  diff = auto
  status = auto
  branch = auto
[user]
  name = David Boclé
  email = bcldvd@gmail.com
[alias]
  ci = commit
  co = checkout
  st = status
  br = branch
[github]
  user = bcldvd
```


## Node

```
sudo apt-get install nodejs
sudo apt-get install npm
```

