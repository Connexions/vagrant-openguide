# Requirements
Use the following links to download and install the necessary software
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

# Clone OpenGuide Vagrant Box
If this is your first time loading the openguide vagrant box then you will need to register an account with [Atlas Hashicorp] (https://atlas.hashicorp.com/account/new) to have access to the vagrant box image. You will then need to email me at zach.roehr@rice.edu with your Atlas username and I will add you as a collaborator on Atlas. You will NOT be able to complete the rest of the steps without me assigning you as a collaborator on Atlas.

Clone the vagrant-openguide repository
```sh
git clone https://github.com/Connexions/vagrant-openguide.git openguide
cd openguide
```
## First time users
After creating an account with Atlas, you will need to run ``vagrant login``.
This will ask you for the username and password you created with Atlas.

## All Users
Make sure you are in the project directory and run ``vagrant up``
```sh
cd openguide
vagrant up
```
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

# Clone OpenGuide Projects
Make sure you are in your project directory and clone the following into ``www/``:
* [OpenGuide Backend] (https://github.com/Connexions/openguide_backend)
* [OpenGuide Frontend] (https://github.com/Connexions/openguide_frontend)

Delete the default ``openguide_frontend`` directory and all of its contents
```sh
cd www/
sudo rm -r openguide_frontend
```
```sh
git clone https://github.com/Connexions/openguide_backend.git
git clone https://github.com/Connexions/openguide_frontend.git
```
# Install Ember-cli dependencies
```sh
cd openguide_frontend
npm install && bower install
```
You should now see the production version of OpenGuide at openguide.dev

# Developing Locally
All files within the ``www/`` directory are automatically synced on ``vagrant up``.
To develop locally with automatic reload make sure you are in the ``www/openguide_frontend`` directory and run ``ember serve`` from your HOST machine.

Go to [localhost:4200] (http://localhost:4200) in your browser.
