# Provisioning with Vagrant

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
