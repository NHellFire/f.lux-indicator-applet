f.lux indicator applet
======================
Better lighting for your computer
Learn more here: https://justgetflux.com/

f.lux indicator applet is an indicator applet to control xflux: an application
that makes the color of your computer's display adapt to the time of day, warm
at nights and like sunlight during the day.

INSTALLATION FROM SOURCE CODE
--------
###STEP 1 Install the dependencies

Fedora:

```
sudo yum install gnome-python2-gconf pexpect python-appindicator git
```

Debian:

```
sudo apt-get install python-gconf python-pexpect python-appindicator git fakeroot
```

###STEP 2 Download the source code

```
git clone https://github.com/Kilian/f.lux-indicator-applet.git
cd f.lux-indicator-applet
```

###STEP 3 Download xflux (not required for Debian/Ubuntu)

32bit:

```
wget https://justgetflux.com/linux/xflux-pre.tgz
tar zxvf xflux-pre.tgz
```

64bit:

```
wget https://justgetflux.com/linux/xflux64.tgz
tar zxvf xflux64.tgz
```


###STEP 4 Build and install

Debian/Ubuntu:

```
dpkg-buildpackage -rfakeroot -b -uc -us
sudo dpkg -i ../flux_1.1.8_all.deb (check filename)
```

Other distros:

```
python setup.py build
sudo python setup.py install
cd ..
rm -r f.lux-indicator-applet
```
