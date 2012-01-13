## DESCRIPTION

Builds an AEgir environment and site on top of a Vagrant vm.

## REQUIREMENTS

* [This project's source](https://github.com/xforty/vagrant-aegir)
* Not windows (haven't tested it yet, but you can try)
* Ruby >= 1.9.2 (do yourself a favor and use
  [rvm](http://beginrescueend.com/) to manage your ruby environment)
* [VirtualBox](http://www.virtualbox.org/)
* [vagrant](http://www.vagrantup.com/) gem
* [chef](http://wiki.opscode.com/) gem
* [librarian](https://github.com/applicationsonline/librarian) gem

## BASIC USAGE

1. Start on the host by provisioning and logging into a vm:

        host$ git clone git://github.com/xforty/vagrant-aegir.git
        host$ cd vagrant-aegir
        host$ librarian-chef install
        host$ vagrant up

2. After AEgir installs your will see 

        Aegir is now installed. You can visit it at http://localhost/user/reset/1/1326478208/3ce5671f68069a2807136c47ae6042c9
        ************************************************************************
        Aegir frontend bootstrap correctly, operation was a success!

   You need to append the port :4567 for it to work.

        http://localhost:4567/user/reset/1/1326478208/3ce5671f68069a2807136c47ae6042c9

3. You can login the guest and sudo to aegir

        host$ vagrant ssh
        guest$ sudo su - aegir

## TODO

* Consider using an existing aegir cookbook.

--------------------------------------------------------------------- 
Maintained by [xforty technologies](http://www.xforty.com)
