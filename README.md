# VeriFolio Virtual Machine

## Vagrant base box

Inside the `packer` directory, there are [Packer](http://www.packer.io/) templates and scripts to generate a base box for VeriFolio.

To build the base box:

    $ cd packer/
    $ packer build arch-template.json

More information is available in `packer/README.md`.

## Vagrant box

To import the generated box into Vagrant:

    $ vagrant box add arch packer/packer_arch_virtualbox.box
    
Launch and provision the machine:

    $ vagrant up