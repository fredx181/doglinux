---
layout: menu
title: DebianDog Wheezy
image: css/wheezy.png
---     

---
<br> 
[DebianDog-Wheezy forum thread.](http://murga-linux.com/puppy/viewtopic.php?t=93225){:target="_blank"}   
[DebianDog-Wheezy updates and  fixes information.](https://github.com/DebianDog/Wheezy/blob/master/Bugs-and-Fixes.md){:target="_blank"}   
[Extra squashfs modules](https://github.com/DebianDog/Wheezy/releases/tag/v0.1){:target="_blank"}

DebianDog is a small Debian Live CD shaped to look like Puppy and act like Puppy. Debian structure and Debian behaviour are untouched and Debian documentation is 100% valid for DebianDog. You have access to all Debian repositories using apt-get or synaptic.

It is not Puppy linux and it has nothing to do with Puppy based on Debian. Downloading DebianDog be ready to learn different package manager and different system setup in Debian manner. 

[Boot method](https://github.com/DebianDog/Jessie/wiki/Boot-methods){:target="_blank"} - [Utilities thread](http://www.murga-linux.com/puppy/viewtopic.php?t=93391){:target="_blank"} - [HowTo thread](http://murga-linux.com/puppy/viewtopic.php?t=93496){:target="_blank"}.

Both systemd and sysvinit included with choice to boot the one you prefer. If you need to edit the boot code keep in mind adding **init=/bin/systemd** will boot with systemd. Removing **init=/bin/systemd** will boot with sysvinit.

DebianDog is set to autologin as root. If you like to use it as multiuser system it is recommended to start XDM login manager (available only in Jwm version). Just type in terminal **xdm-start** and reboot. **xdm-stop** will reverse back autologin as root.
In OpenBox version you can install this [slim deb package](http://smokey01.com/saintless/DebianDog/Packages/Extra/slim_1.3.4-2-ddwheezy_i386.deb) and use menu System -> Start/Stop Slim display-manager. If you like to change the default autologin as root to autologin as user [read here how to do it.](http://murga-linux.com/puppy/viewtopic.php?p=850601#850601){:target="_blank"}

Login details:   
**root** with password **root**   
**puppy** with password **puppy**

Two versions available for download (also attached here):   
1. From saintless:    
[DebianDog-Wheezy-jwm_icewm-2015-09-02.iso](https://github.com/DebianDog/Wheezy/releases/download/v1.0/DebianDog-Wheezy-jwm_icewm-2015-09-02.iso) - 119 Mb.    
Kernel 3.2.0-4-486 (for older PC).   
[DebianDog-Wheezy-jwm_icewm-2015-09-02-PAE.iso](https://github.com/DebianDog/Wheezy/releases/download/v1.0/DebianDog-Wheezy-jwm_icewm-2015-09-02-PAE.iso) - 141 Mb.   
Kernel-3.16.0-4-686-pae (for modern PC).   

Default WM - JWM with option to switch to IceWM.   
Default File Manager - XFE with option to use Rox.   
Default Internet Browser - Dillo.   

![Jwm version](https://github.com/DebianDog/Jessie/blob/master/screenshots/DebianDog-Wheezy-jwm-icewm.jpg?raw=true)   
2. From fredx181:      
[DebianDog-Wheezy-openbox_xfce-2015-09-02.iso](https://github.com/DebianDog/Wheezy/releases/download/v1.0/DebianDog-Wheezy-openbox_xfce-2015-09-02.iso) - 159 Mb.   
Kernel-3.2.0.4-486 (for older PC).   
[DebianDog-Wheezy-openbox_xfce-2015-09-02-PAE.iso](https://github.com/DebianDog/Wheezy/releases/download/v1.0/DebianDog-Wheezy-openbox_xfce-2015-09-02-PAE.iso) - 180 Mb.   
Kernel-3.16.0-4-686-pae  (for modern PC).   

Default WM - OpenBox with XFCE.   
Default File Manager - Thunar with option to use Rox or XFE.   
Default Internet Browser - Firefox.   

![OpenBox version](https://github.com/DebianDog/Jessie/blob/master/screenshots/DebianDog-Wheezy-openbox-xfce.jpg?raw=true)

[md5sum check](https://github.com/DebianDog/Wheezy/blob/master/md5sum){:target="_blank"}

To test DebianDog for first time you need to burn it on CD and boot from it, or use DebianDog-installer [click here to download and extract the archive](https://github.com/DebianDog/Wheezy/releases/download/v1.0/DebianDog-Installer.tar.gz) - working from most linux systems to make frugal install to HDD or USB,  or to extract /live folder on top of a partition or USB and edit grub menu.lst.

The iso is hybrid and you can make bootable usb using dd command. This option is for users with more experience and  makes the usb partition with DebianDog files read-only without option to replace the included boot menu with custom menu entry.
[Hybrid-iso to usb example using /dev/sdb flash drive posted here.](http://murga-linux.com/puppy/viewtopic.php?p=849026#849026){:target="_blank"}

**It is recommended to use DebianDog-installer working on most linux systems - [attached here](https://github.com/DebianDog/Wheezy/releases/download/v1.0/DebianDog-Installer.tar.gz).**

To keep the size small as possible all **/usr/share/locale** files for the included packages are moved in separate squashfs module [00-locale-files-openbox_xfce.squashfs](https://github.com/DebianDog/Wheezy/releases/download/v0.1/00-locale-files-openbox_xfce.squashfs)  and [00-locale-files-jwm-icewm.squashfs](https://github.com/DebianDog/Wheezy/releases/download/v0.1/00-locale-files-jwm-icewm.squashfs) available for download from sfs-get or from **[here.](https://github.com/DebianDog/Wheezy/releases/v0.1/)**
In case you like to change the localization install **locales** and load the module or place it inside /live/image/live to be loaded at boot time.
You can also install localepurge and copy only the language files you need from the squashfs module in /usr/share/locale directory to save space in the future.
Included [menu-openbox](http://murga-linux.com/puppy/viewtopic.php?p=861811#861811){:target="_blank"} from Fred with localisation support (the default menu displays categories and menu entries only in English). In case you like to change the localisation type menu-openbox in terminal or start it from System -> Menu Openbox.
More information about changing localization read [here](http://murga-linux.com/puppy/viewtopic.php?p=851852#851852){:target="_blank"}, [here](http://murga-linux.com/puppy/viewtopic.php?p=851889#851889){:target="_blank"} and [here.](http://murga-linux.com/puppy/viewtopic.php?p=851899#851899){:target="_blank"}

DebianDog has tools similar to Puppy. You can create easy separate squashfs modules and remaster the system with all personal changes.
You can even use/convert pet packages and sfs files from Puppy but it is not recommended if you like to keep well working apt-get/Synaptic package manager (which is the main advantage using DebianDog). 

I like to give my Thanks to Smokey and KazzaMozz for hosting DebianDog project [here](http://smokey01.com/saintless/), [here](http://kazzascorner.com.au/saintless/DebianDog/){:target="_blank"} and [here](https://www.mediafire.com/folder/9d9nm6np2drmq/DebianDog_by_Saintless){:target="_blank"}, to Debian team for keeping Debian such flexible system, to http://murga-linux.com/puppy/index.php and http://github.com for the opportunity to work on this project, to puppy linux forum members working on DebianDog development: Fred (fredx181), Terry (sunburnt), William (mcewanw), Sergey (sklimkin), and for the valuable advices to: jbv, sfs, catsezmoo, big_bass, emil, dancytron, anikin from our forum
and dzz from www.debianuserforums.org
And  to Sickgut for his original idea that made possible DebianDog to exist.

**Related links:**   
[Lumina Desktop for DebianDog and MintPup](https://github.com/MintPup/Lumina){:target="_blank"}   
[Setting up Chinese fonts github wiki from limelime](https://github.com/limelime/DebianDog/wiki/Chinese-characters-support-in-Iceweasel-Firefox-and-in-the-console-terminal){:target="_blank"}   
[DebianDog wireless LAN HowTo thread](http://murga-linux.com/puppy/viewtopic.php?p=833212#833212){:target="_blank"}   
[MintPup-Trusty LTS](https://github.com/MintPup/MintPup-Trusty){:target="_blank"}   
[DebianDog-Jessie](https://github.com/DebianDog/Jessie){:target="_blank"}   
[DebianDog-Wheezy](https://github.com/DebianDog/Wheezy){:target="_blank"}   
[DebianDog-Squeeze](https://github.com/MintPup/DebianDog-Squeeze){:target="_blank"}   
[Retro-Debian](https://github.com/MintPup/Retro-Debian){:target="_blank"}   
[Kingston wps-office sfs module](http://murga-linux.com/puppy/viewtopic.php?p=862907#862907){:target="_blank"}   
[Infinality fonts packages for Debian Wheezy (thanks to Keisha)](http://murga-linux.com/puppy/viewtopic.php?p=832727#832727){:target="_blank"}   
[DebianDog HowTo thread](http://murga-linux.com/puppy/viewtopic.php?t=93496){:target="_blank"}   
[DebianDog Utilities thread](http://www.murga-linux.com/puppy/viewtopic.php?t=93391){:target="_blank"}   
[Systemd boot information](http://murga-linux.com/puppy/viewtopic.php?p=777990#777990){:target="_blank"}   
[Install Spotify on Debian/DebianDog](http://www.murga-linux.com/puppy/viewtopic.php?p=804004#804004){:target="_blank"}   
[DebianDog + Blue Pup Quirky Tahr Dual Boot USB Stick How-To](http://murga-linux.com/puppy/viewtopic.php?t=95139){:target="_blank"}   
[How To Make A Network Storage NAS Appliance With DebianDog and OpenMediaVault](http://murga-linux.com/puppy/viewtopic.php?t=95249){:target="_blank"}   
[Use old Skype version after 01.08.2014](http://murga-linux.com/puppy/viewtopic.php?p=793486#793486){:target="_blank"}   