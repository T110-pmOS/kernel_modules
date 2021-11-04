# kernel_modules
Kernel modules 3.4.5

Standard path

`/lib/modules/3.4.5`

Modules need be loaded after system booted:

```
sudo depmod

sudo echo $'sd8xxx\nmlan\ngalcore' > /etc/modules-load.d/load-generic.conf

```

If sd8xxx and mlan loads too early it will not give interface.

mbt8xxx bluetooth module might crash the system.

Blacklist them in:

`sudo echo $'sd8xxx\nmlan\nmbt8xxx' >> /etc/modprobe.d/blacklist.conf`