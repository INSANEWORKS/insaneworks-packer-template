insaneworks-packer-template
=============

FreeBSD 13 aarch64 / AlmaLinux 9 aarch64 + Parallels

## Packer Build for Parallels

```
cd freebsd13-aarch64 or almalinux9-aarch64
packer validate [  AlmaLinux_8.json | FreeBSD13.json ]
VERSION=v20210810 packer build [ FreeBSD12.json | FreeBSD13.json ]
```

## Add Vagrant Box

```
vagrant box add BOXNAME INSANEWORKS-AlmaLinux-9-aarch64-v20220810-parallels.box
vagrant box add BOXNAME INSANEWORKS-FreeBSD-13-aarch64-v20220810-parallels.box
```

## Atlas a.k.a Vagrant Cloud


```
mkdir vagrant-virtualmachine
cd vagrant-virtualmachine

vagrant init insaneworks/almalinux9-aarch64
or
vagrant init insaneworks/freebsd13-aarch64
```

```
vagrant up
```


## or Public URL Init


```
mkdir centos
cd centos
vagrant init INSANEWORKS-AlmaLinux-9-aarch64-v20210810 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-AlmaLinux-9-aarch64-v20220810-parallels.box
or
vagrant init INSANEWORKS-FreeBSD-13-aarch64-v20210810 https://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-FreeBSD-x86_64-aarch64-v20220810-vmware.box
```

```
vagrant up
```

## or Edit Vagrantfile (Vagrant 1.5.0 or Higher)

```diff
   # please see the online documentation at vagrantup.com.

   # Every Vagrant virtual environment requires a box to build off of.
-  config.vm.box = "base"
+  config.vm.box "insaneworks/freebsd13-aarch64" or "insaneworks/almalinux9-aarch64"

   # Create a forwarded port mapping which allows access to a specific port
   # within the machine from a port on the host machine. In the example below,
```

vagrant up
