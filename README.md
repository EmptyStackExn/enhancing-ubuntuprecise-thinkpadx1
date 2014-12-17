Enhancing Ubuntu 12.04 LTS on a ThinkPad X1 machine
==============

*Design* and *User Experience* (UX/UI) are topics that developers should never underestimate. In this way, customizing your favorite Linux distribution should give you a better work experience. Here is a cheatsheet that gathers tips I applied to [Ubuntu 12.04 LTS (Precise Pangolin)](http://releases.ubuntu.com/12.04/) with [GNOME 3 Fallback Session (Classic)](https://launchpad.net/ubuntu/precise/+package/gnome-session-fallback) on my [Lenovo ThinkPad X1](http://www.lenovo.com/mp/x1/index.html).

![Alt text](https://raw.githubusercontent.com/EmptyStackExn/enhancing-ubuntuprecise-thinkpadx1/master/images/desktop.png "A screenshot of my desktop")

----------------------


Plug your [Android device](http://www.android.com/) with [MTP](http://www.androidcentral.com/ics-feature-mtp-what-it-why-use-it-and-how-set-it) protocol
----------------------
You can plug your device and automatically get it mounted without performing any commands on 12.04 with a [GVFS](http://library.gnome.org/misc/release-notes/2.22/#sect:gvfs-gio) MTP backend provided by [langdalepl](https://launchpad.net/~langdalepl/+archive/ubuntu/gvfs-mtp) as well as newer versions of Ubuntu.

 1. Add the following PPA repository: `sudo add-apt-repository ppa:langdalepl/gvfs-mtp`
 2. Update your packages: `sudo apt-get update && sudo apt-get upgrade`


Encrypt your Hard Drive ([howtogeek.com](http://www.howtogeek.com/116032/how-to-encrypt-your-home-folder-after-installing-ubuntu/))
----------------------
Research centers and governmental agencies [recommend research data encryption](https://aresu.dsi.cnrs.fr/spip.php?rubrique99) to avoid sensitive information leakage. For this reason, [eCryptfs](http://ecryptfs.org/) made it easy and may not be greedy as the [Intel® Core™ i5-2520M Processor](http://ark.intel.com/fr/products/52229/Intel-Core-i5-2520M-Processor-3M-Cache-up-to-3_20-GHz) provides hardware [Intel® AES-NI](http://www.intel.com/content/www/us/en/architecture-and-technology/advanced-encryption-standard--aes-/data-protection-aes-general-technology.html?_ga=1.149398710.168035845.1418680010) support.

 1. Install required tools: `sudo apt-get install ecryptfs-utils cryptsetup`
 2. Create a temporary user with `Administrator` rights
 3. Log on it and run `sudo ecryptfs-migrate-home -u [user]`
 4. Encrypt the swap partition: `sudo ecryptfs-setup-swap`

----------------------


Monitor Degradation and Failure of your Hard Drive
----------------------
  - manual start/stop of `smartd`: `sudo /usr/local/etc/init.d/smartd start`
  - http://www.cyberciti.biz/tips/monitoring-hard-disk-health-with-smartd-under-linux-or-unix-operating-systems.html
  - http://www.linuxjournal.com/content/know-when-your-drives-are-failing-smartd
  - http://www.ibiblio.org/elemental/howto/disk-monitoring.html
  - http://www.fibrevillage.com/storage/46-how-to-configure-smartd-to-monitor-hard-disk-health-under-linux

----------------------


Logon with fingerprint
----------------------
  - tutorial for X1: http://fcns.eu/2012/04/29/fingerprint-reader/
  - http://www.ullrich-online.cc/fingerprint

----------------------


Use Flatten Design
----------------------
  - flatten icons made by NitruxSA for GNOME: https://github.com/NitruxSA/flattr-icons
  - window decoration with [Compiz/Emerald](http://wiki.compiz.org/Decorators/Emerald): http://gnome-look.org/content/show.php/Elegant+Brit?content=74553
  - some discussions: http://bits.blogs.nytimes.com/2013/04/23/the-flattening-of-design/?_r=0

----------------------


Get the `Menu` key back
----------------------
  - http://efod.se/writings/linuxbook/html/caps-lock-to-ctrl.html


----------------------


Add System Indicators on GNOME Panel
----------------------


----------------------

Disclaimer
----------------------
THE PROVIDER MAKES NO REPRESENTATIONS ABOUT THE SUITABILITY, USE, OR PERFORMANCE OF THESE TIPS OR ABOUT ANY CONTENT OR INFORMATION MADE ACCESSIBLE BY THESE, FOR ANY PURPOSE.

Hai Nguyen Van <nguyen-van@lri.fr>



