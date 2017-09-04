# Purpose

Install and setup a virtual machine as development environment to start with hyperledger-fabric.

* installs go
* installs docker
* installs docker-compose
* installs nodejs and npm
* hyperledger-fabric plattform specific binaries are installed and are added to the $PATH
* content of go path is accessable from host

# Prerequisites

The following tools have to be installed on your operating system:
* Vagrant
* VirtualBox
* VirtualBox Guest Additions

The easiest way for me to install VirtualBox Guest Additions was to install the vagrant-vbguest plugin.

    vagrant plugin install vagrant-vbguest

# Next steps

E.g. start with the hyperledger-fabric samples from http://hyperledger-fabric.readthedocs.io/en/latest/samples.html and clone them into the /home/vagrant/gopath folder.

# Run the fabcar example from hyperledger-fabric samples

I run into some issues if I try to install the node packages referenced within the fabcar sample.
My solution was to install node-pre-gyp and semver globally and then run npm install from the fabcar directory with the --no-bin-links option.
    
    vagrant@jessie:~$ sudo npm install node-pre-gyp semver -g
    vagrant@jessie:~/gopath/fabric-samples/fabcar$ npm install --no-bin-links
