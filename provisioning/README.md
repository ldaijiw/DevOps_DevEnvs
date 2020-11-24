# Vagrant and VM Provisioning

Provisioning is a way to provide VMs with instructions, variables, files, and folders.

This gives the ability to set up a machine to a specific state when turned on.

## Sending Files/Folders to VM

In the Vagrantfile add to the configuration

```ruby
# upload files to VM
config.vm.provision "file", source: "C:\\path\\to\\file", destination: "$HOME/new/path"

```
**LINUX IS CASE SENSITIVE BUT WINDOWS ISN'T, MAKE SURE PATH STRING IS CORRECT**

Then after reloading with ``vagrant reload``

Provision the files/folders with
```bash
vagrant provision
```
