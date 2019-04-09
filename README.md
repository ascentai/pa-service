# pa-service
Pulse audio service allowing to launch the pulseaudio system-wide on boot.

## When to use 
Works great on headless system where pulse audio server is necessary.

Read the Pulse audio guideline on system-wide before usage:
- https://www.freedesktop.org/wiki/Software/PulseAudio/Documentation/User/SystemWide/
- https://www.freedesktop.org/wiki/Software/PulseAudio/Documentation/User/WhatIsWrongWithSystemWide/

## Getting prepared
On ubuntu 16.04.5 LTS
```
$ sudo apt-get install build-essential
$ sudo apt-get install dh-systemd
```

## Build the package 
```
$ mkdir deb-build-dir && cd deb-build-dir
$ git clone git@github.com:ascentai/pa-service.git && cd pa-service
$ dpkg-buildpackage -us -uc
$ cd ../ && ls -la | grep *.deb
```

## Install
```
$ sudo dpkg -i pa-service_0.1.0_all.deb
```
