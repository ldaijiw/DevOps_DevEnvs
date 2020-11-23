# First Dev Environment

## VIRTUAL BOX

Creator of Virtual Machines

## VAGRANT

Declarative way (code) to build VM VirtualBox (or others)


**VAGRANT BOXES**

Pre loaded Vagrantfiles that create VMs, usually just an OS

[Discover Vagrant Boxes](https://app.vagrantup.com/boxes/search)

Ubuntu  
- Open source Linux OS  
- Ubuntu with GUI  
- Ubuntu headless (only interact through terminal)  



## Main Commands

- In cwd, initialise vagrant to create a vagrant file
```bash
vagrant init
```

- Alternatively can specify vagrant box with
```bash
vagrant init <box> (e.g. ubuntu/xenial64)
```

- Start vagrant with
```bash
vagrant up
```
- SSH into VM with
```bash
vagrant ssh
```

- Stop Vagrant with
```bash
vagrant halt
```

- Reload vagrant with
```bash
vagrant reload
```

- Destroy Virtual box with 
```bash
vagrant destroy
```

- Install Vagrant Plugin
```bash
vagrant plugin-install <plugin>
```
	- ``vagrant-hostsupdater`` (Plugin to enable hostname configuration of VM)[https://github.com/agiledivider/vagrant-hostsupdater]

### Linux Commands

- Find list of packages to update
```bash
sudo apt update
```

- To install updates
```bash
sudo apt upgrade
```

- Install package
```bash
sudo apt install <package>
```