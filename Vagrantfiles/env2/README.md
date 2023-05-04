# Environment 2

The purpose of this Vagrantfile is to provide two, ready to use RedHat Enterprise Linux 9 VM instances.


## How to provision this VM

The blueprint supports Hyper-V, VirtualBox and VMware Workstation hypervisor backends, simply provision and connect to these VMs using Vagrant.

```bash
vagrant up
vagrant ssh client
vagrant ssh server
```