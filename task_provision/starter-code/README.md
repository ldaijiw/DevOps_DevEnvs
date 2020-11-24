# Provisioning with Vagrant

## Core Sections of Provisioning

There are some actions that are core to provisioning.  
**These concepts are essential to all tools/languages (agnostic)**
- Making files available
- Being able to run commands/scripts
- Injecting environment variables

### Sync files with VM

Allows to send files and sync them into VM, in order to make code and other necessary files available
```ruby
Vagrant.configure("2") do |config|
	config.vm.box = "ubuntu/bionic64"
	config.vm.network "private_network", ip: "192.168.10.100"
	config.hostsupdater.aliases = ["development.local"]

	config.vm.synced_folder "environment/", "/startercode/environment"
	config.vm.synced_folder "app/", "/startercode/app"

end
```

### Running Bash Script

Bash script to install packages, alter files, do actions in linux VM when running ``vagrant up``

This will allow to set up the machine to a state that is desirable and automate processes

- Create ``provision.sh`` file
- Include ``#!/bin/bash`` at top of file so it runs as Bash script
- Include in vagrant file
```ruby
	# run provision cript
	config.vm.provision "shell", path: "environment/provision.sh"
```

## When given a project to create an environment

WHen given a project, few questions to ask
- What language is it in
- Is there a framework to install (rails, flask, django, wordpress, etc.)
- Any specific packages
	- If so is there a list? (Gemfile, requirements.txt)
- Any tests

## Gem and Bundler vs. PIP and Packages

- Gems are packages in ruby or dependencies
- Bundler is ruby's package manager
```
gem install bundler
```
- Gemfile keeps a list of dependencies to be installed
	- Go to folder with Gemfile
```
bundle
```

- To install gems from Gemfile, use
```
bundle install
```

**Ruby's testing framework is rspec**

- Go to folder with Rakefile
	- Run tests with
```
rake spec
```

**JS package manager is npm (node package manager)**


## For this Project

**What language is it in?**

- Code is in JS
- There are some tests in ruby and rspec

**IS there a framework to install?**

- No only testing framework, rspec

**Any specific packages?**

- Yes with environment file, there is a Gemfile with dependencies

**Any tests?**

- Yes, integration tests to run outside VM with ``rake spec``
- There may also be some unit testing in JS inside VM


### Extra Commands

```
sudo systemctl <action> <service>
```
- ``status``
- ``start``
- ``stop``
- ``restart``