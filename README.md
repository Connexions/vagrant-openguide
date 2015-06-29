# Requirements
* [VirtualBox] (https://www.virtualbox.org/wiki/Downloads)
* [Vagrant] (http://www.vagrantup.com/downloads.html) 1.7.2
* ember-cli 0.2.3

# Installing Vagrant
After installing VirtualBox and Vagrant run ``vagrant -v``
If you see
```sh
Installed Version: 1.7.2
Latest Version: 1.7.2
```
then vagrant is installed and working.

# Install and Provision OpenGuide Vagrant Box
Clone the vagrant-openguide repository
```sh
git clone https://github.com/Connexions/vagrant-openguide.git openguide
cd openguide
vagrant up
```
If this is your first time loading the openguide vagrant box then you will need to register an account with [Atlas Hashicorp] (https://atlas.hashicorp.com/account/new) to have access to the vagrant box image.

# Edit Hosts file
You will need to edit the ``/etc/hosts`` file of your HOST's machine.
```sh
sudo nano /etc/hosts
```
Add the following line at the end of the file
```
192.168.33.10 openguide.dev
```
Now go to [openguide.dev] (http://openguide.dev/) to see your new VM running!

# Clone OpenGuide projects
