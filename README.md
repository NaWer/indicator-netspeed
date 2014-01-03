Network speed indicator for Unity
=================================

![](https://raw.github.com/mgedmin/indicator-netspeed/master/screenshot.png)

Usage
-----

```
sudo apt-get install build-essential libgtop2-dev libgtk-3-dev libappindicator3-dev git-core
git clone git://github.com/mgedmin/indicator-netspeed.git
cd indicator-netspeed
make
./indicator-netspeed
```


Bugs
----

The indicator keeps changing size to match the text, which pushes other
indicators left and right all the time, which makes it very annoying and
unusable.

It's not packaged, so installation procedure is very inconvenient.

Network-idle icon is a link to network-transmit-receive icon (see https://bugs.launchpad.net/ubuntu/+source/humanity-icon-theme/+bug/611336).
```
You can use network-idle.svg (Ubuntu Ambiance theme):
sudo rm /usr/share/icons/ubuntu-mono-dark/status/22/network-idle.svg
sudo cp network-idle.svg /usr/share/icons/ubuntu-mono-dark/status/22/
```


Credits
-------

Written by Marius Gedminas <marius@gedmin.as>

Contributors:

- Tobias Brandt <tob.brandt@gmail.com> 
