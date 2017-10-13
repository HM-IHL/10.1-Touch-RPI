# 10.1-Touch-RPI
Python Touchscreen Right Click

This project implements right click functionality using a touchscreen on an Ubuntu system using the [Python evdev](https://github.com/gvalkov/python-evdev) library. Because of unity's deep integration with multitouch gestures, it disallows many other systems from implementing basic gestures that (IMHO) are missing from the default multitouch gestures. This script will not override unity's gestures, but fill in some missing ones, working alongside unity's multitouch system. (Also tested in gnome-shell given gnome-shell's incomplete implementation of right click touch)

Implemented gestures

Two gesture options have been implemented for right click:

1 finger longpress * Standard operation is to open menu after finger is lifted. * Temporary workaround will bring up right click while still pressing
2 finger tap
Setting up script

To modify the delay for your right click, open the script in a text editor and modify the self.click_delay variable, the default is 1.5 seconds.

To install please follow the instructions below:

1) Install Dependencies:
sudo apt-get install libts-bin evtest xinput python-dev python-pip

    then:

    sudo pip install pyuserinput

2) Clone repository:
sudo git clone https://github.com/HM-IHL/10.1-Touch-RPI

3) Change Directory:
cd 10.1-Touch-RPI

4) Install python evdev:
sudo python setup.py install

5) Now you can run the software:
sudo python Python-Touchscreen-RightClick
