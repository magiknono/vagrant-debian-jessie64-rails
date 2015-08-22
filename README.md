# VAGRANT Starter Kit
My Vagrant personnal base box kit debian 8 powered with ruby on rails env

## Requirements

- Virtualbox 5.0.2
- Vagrant_1.7.4_x86_64.deb
- Need to have the package.box in ~/VagrantBox/Box

## Featuring

- Debian 8.1 amd64
- VirtualBox GuestAdditions 5.0.2
- rbenv with ruby 2.2.3
- oh-my-zsh
- sqlite3
- postgresql
- git
- gems : rails bundler colored pg
- ssh and http redirect to the host
- a demo rails "helloword" app
- fr local
- nodejs
- vim
- HardDisk of only 4.5 Go extensible to 40

## Installation

Clone the repo in ~/VagrantBox/env
```
cd ~/VagrantBox/env
vagrant up
```

## Starting the demo app to see env variables

```
ssh -p 2222 vagrant@127.0.0.1
cd myapps/helloworld
rails s -b 0.0.0.0
```

GO to your host and open your favorite browser and see http://127.0.0.1:3000

## Editing your rails file in your host

All new apps in the guest myapps directory will be synced with the host ~/VagrantBox/env/myapps

```
ssh -p 2222 vagrant@127.0.0.1
cd myapps
rails new sqlite3demoapp
exit
ls ~/VagrantBox/env/myapps/sqlite3demoapp
atom .
```

## Info

login/passwd :
Linux
 - root/vagrant
 - vagrant/vagrant
Postgresql
 - vagrant/vagrant (need to edit config/database.yml for rails postgresql app !)

uname -a =
 Linux debian-jessie64-rails 3.16.0-4-amd64 #1 SMP Debian 3.16.7-ckt11-1+deb8u3 (2015-08-04) x86_64 GNU/Linux

## After install

You have to personalize with your dotfile and install your github env if needed

## TO DO

Need to update with a shell provisioner script for automation
