centos-packer
=============

CentOS 6.5 x86_64 + Chef for Packer

## Packer Build for VirtualBox

```
packer validate CentOS_6.5.json
packer build -only virtualbox CentOS_6.5.json
```

## Add Vagrant Box

```
box add BOXNAME INSANEWORKS-CentOS-6.5-x86_64-v20131201.box
```

## Vagrant up

```
mkdir centos
cd centos
vagrant init BOXNAME
vi Vagrantfile
vagrant up
```

## or Public URL Init

```
mkdir centos
cd centos
vagrant init INSANEWORKS-CentOS-6.5-x86_64-v20131201 http://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-CentOS-6.5-x86_64-v20131201.box
vagrant up
```

## or Edit Vagrantfile

```diff
   # please see the online documentation at vagrantup.com.

   # Every Vagrant virtual environment requires a box to build off of.
-  config.vm.box = "base"
+  config.vm.box = "INSANEWORKS-CentOS-6.5-x86_64-v20131201"

   # The url from where the 'config.vm.box' box will be fetched if it
   # doesn't already exist on the user's system.
-  # config.vm.box_url = "http://domain.com/path/to/above.box"
+  config.vm.box_url = "http://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-CentOS-6.5-x86_64-v20131201.box"

   # Create a forwarded port mapping which allows access to a specific port
   # within the machine from a port on the host machine. In the example below,
```

```
vagrant up
```

Enjoy!!
