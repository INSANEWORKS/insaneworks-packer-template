insaneworks-packer-template
=============

CentOS 6 - 8 / FreeBSD 12 x64 + VirtualBox / VMWare for Packer Template

## Packer Build for VirtualBox

```
cd centos6 or centos7 or centos8 or freebsd12
packer validate [ CentOS_6.json | CentOS_7.json | CentOS_8.json | FreeBSD12.json ]
VERSION=v20200910 packer build [ -only virtualbox-iso | -only vmware-iso ]  [ CentOS_6.json | CentOS_7.json | CentOS_8.json | FreeBSD12.json ]
```

## Add Vagrant Box

```
vagrant box add BOXNAME INSANEWORKS-CentOS-6-x86_64-v20200910-virtualbox.box
vagrant box add BOXNAME INSANEWORKS-CentOS-7-x86_64-v20200910-virtualbox.box
vagrant box add BOXNAME INSANEWORKS-CentOS-6-x86_64-v20200910-virtualbox.box
vagrant box add BOXNAME INSANEWORKS-FreeBSD-12-x86_64-v20200910-virtualbox.box
or
vagrant box add BOXNAME INSANEWORKS-CentOS-6-x86_64-v20200910-vmware.box
vagrant box add BOXNAME INSANEWORKS-CentOS-7-x86_64-v20200910-vmware.box
vagrant box add BOXNAME INSANEWORKS-CentOS-6-x86_64-v20200910-vmware.box
vagrant box add BOXNAME INSANEWORKS-FreeBSD-12-x86_64-v20200910-vmware.box
```

## Atlas a.k.a Vagrant Cloud

```
mkdir vagrant-virtualmachine
cd vagrant-virtualmachine

vagrant init insaneworks/centos6
or
vagrant init insaneworks/centos7
or
vagrant init insaneworks/centos8
or
vagrant init insaneworks/freebsd12

vagrant up
```


## or Public URL Init

```
mkdir centos
cd centos
vagrant init INSANEWORKS-CentOS-6-x86_64-v20200910 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-CentOS-6-x86_64-v20200910-virtualbox.box
vagrant init INSANEWORKS-CentOS-7-x86_64-v20200910 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-CentOS-7-x86_64-v20200910-virtualbox.box
vagrant init INSANEWORKS-CentOS-8-x86_64-v20200910 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-CentOS-8-x86_64-v20200910-virtualbox.box
vagrant init INSANEWORKS-FreeBSD-12-x86_64-v20200910 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-FreeBSD-12-x86_64-v20200910-virtualbox.box
or
vagrant init INSANEWORKS-CentOS-6-x86_64-v20200910 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-CentOS-6-x86_64-v20200910-vmware.box
vagrant init INSANEWORKS-CentOS-7-x86_64-v20200910 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-CentOS-7-x86_64-v20200910-vmware.box
vagrant init INSANEWORKS-CentOS-8-x86_64-v20200910 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-CentOS-6-x86_64-v20200910-vmware.box
vagrant init INSANEWORKS-FreeBSD-12-x86_64-v20200910 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-FreeBSD-12-x86_64-v20200910-vmware.box
vagrant up
```

## or Edit Vagrantfile (Vagrant 1.5.0 or Higher)

```diff
   # please see the online documentation at vagrantup.com.

   # Every Vagrant virtual environment requires a box to build off of.
-  config.vm.box = "base"
+  config.vm.box = "insaneworks/centos" or "insaneworks/centos7" or "insaneworks/centos8" or "insaneworks/freebsd12"

   # Create a forwarded port mapping which allows access to a specific port
   # within the machine from a port on the host machine. In the example below,
```

```
vagrant up11.5.5
```
