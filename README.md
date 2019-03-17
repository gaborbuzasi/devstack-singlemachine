# DevStack on Single Machine using Zun
Requirements for setting up a single machine DevStack instance with docker support running on Ubuntu 16.04


### Steps
1. Install Ubuntu Server 16.04 on a machine
2. Add separate user for DevStack `sudo useradd -s /bin/bash -d /opt/stack -m stack`
3. Give user sudo privileges by `sudo visudo` and adding the following to the end of the file:
```
stack ALL=(ALL) NOPASSWD: ALL
```
4. Use the above created account `sudo su stack`
5. Download DevStack
`git clone https://git.openstack.org/openstack-dev/devstack`
6. Before running `./stack.sh` create configuration file called **local.conf** as per this repository.
Don't forget to replace password placeholders with actual passwords.
