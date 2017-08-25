# Purpose

    Install and setup a virtual machine as development environment to start with hyperledger-fabrice.

* installs go
* installs docker
* installs docker-compose
* hyperledger-fabrice plattform specific binaries are installed and are added to the $PATH
* content of go path is accessable from host

# Prerequisites

The following tools have to be installed on your operating system:
* Vagrant
* VirtualBox
* VirtualBox Guest Additions

The easiest way for me to install VirtualBox Guest Additions was to install the vagrant-vbguest plugin.

    vagrant plugin install vagrant-vbguest

# Next steps
    E.g. start with the hyperledger-fabrice samples from http://hyperledger-fabric.readthedocs.io/en/latest/samples.html and clone them into the /home/vagrant/gopath folder.
