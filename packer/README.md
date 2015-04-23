Packer Verifolio
================

We provide a [Packer](http://www.packer.io/) template for bootstrapping the Verifolio [Vagrant](http://www.vagrantup.com/)
base box based on [Packer Arch](https://github.com/elasticdog/packer-arch).

[Packer Arch](https://github.com/elasticdog/packer-arch) is a bare bones [Packer](http://www.packer.io/) template and
installation script that can be used to generate a [Vagrant](http://www.vagrantup.com/)
base box for [Arch Linux](https://www.archlinux.org/). The template works
with both the default VirtualBox provider as well as the
[VMware provider](http://www.vagrantup.com/vmware).

Usage
-----

### VirtualBox Provider

Assuming that you already have Packer,
[VirtualBox](https://www.virtualbox.org/), and Vagrant installed, you
should be good to clone this repo and go:

    $ git clone https://github.com/thpani/verifolio-vm.git
    $ cd verifolio-vm/packer/
    $ packer build arch-template.json

Then you can import the generated box into Vagrant:

    $ vagrant box add arch packer_arch_virtualbox.box