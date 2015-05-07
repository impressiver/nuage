Nuage for BBB
=============

A fork of the [Nuage](http://www.arduino-hausautomation.de/nuage/) bridge, which makes an Arduino connected to a Beaglebone Black work like an [Arduino Yún](http://www.arduino.cc/en/Main/ArduinoBoardYun). Including programming via Arduino IDE over a local network.

Currently it builds as a debian pkg, but I plan to make it available for other distros soon.

## super()
>  Nuage (french for cloud) is a port of the Arduino Yún bridge library to Debian (mainly targetted at Raspbian). It should also work on Banana Pi and other single board computers. The primarily supported controller is ATmega328 (16MHz, 5V) as found on Watterotts RPi Shield bridge. ATmega328 on breadboard (3,3V, 8MHz internal) is supported as well. ATmega2560 and ATmega1284 will follow as well.


# Install

## Derpendencies
```
$ apt-get update
$ apt-get dist-upgrade
$ apt-get install build-essential python-dev python-setuptools python-pip python-smbus
$ apt-get install avrdude lua5.1 telnet avahi-utils
$ apt-get install strace lsof curl wget python-flask
$ easy_install -U distribute
$ pip install Adafruit_BBIO
```

## Build from source
```
$ git clone https://github.com/impressiver/nuage.git
$ cd nuage
$ ./build-deb.sh
$ dpkg -i nuage-bridge.deb
$ apt-get install -f
$ vim /etc/nuage/nuage.cfg    # set the correct reset pin (the BBB pin, which is connected to the Arduino reset pin)
```
