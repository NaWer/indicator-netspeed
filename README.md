Network speed indicator for Unity
=================================

![](https://raw.github.com/NaWer/indicator-netspeed/master/screenshot.png)

Simple fork with both up and down

Usage
-----

```
sudo apt-get install build-essential libgtop2-dev libgtk-3-dev libappindicator3-dev git-core
git clone git://github.com/mgedmin/indicator-netspeed.git
cd indicator-netspeed
make
sudo make install
indicator-netspeed &
```

The indicator will be put left of all your other indicators. If this is undesirable, the ordering
index can be changed in gsettings:/apps/indicators/netspeed (use dconf-editor).


TODO
----

* Configuration options only accessible through dconf-editor, add a simple options menu.
* Allow toggling autostart at login.
* Do some magic when interfaces are added or disappear.
* The Makefile is a bit stupid right now and is probably specific to ubuntu.
* It's not packaged, create deb building scripts.

Bugs
----
* The indicator keeps changing size to match the text, which pushes other indicators left and right all the time, which makes it very annoying and unusable.
* On Ubuntu 12.04 : Network-idle icon is a link to network-transmit-receive icon 
  * See https://bugs.launchpad.net/ubuntu/+source/humanity-icon-theme/+bug/611336).
  * You can use network-idle.svg (Ubuntu Ambiance theme) :
```
        sudo rm /usr/share/icons/ubuntu-mono-dark/status/22/network-idle.svg
        sudo cp network-idle.svg /usr/share/icons/ubuntu-mono-dark/status/22/
```

Credits
-------

Originally written by Marius Gedminas <marius@gedmin.as>

Contributors:

- Tobias Brandt <tob.brandt@gmail.com>
- Stefan Bethge (stefan at lanpartei.de)

