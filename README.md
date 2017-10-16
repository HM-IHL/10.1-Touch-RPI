# 10.1-Touch-RPI
Python Touchscreen Right Click

This project implements right click functionality using a touchscreen on an Linux system using the evdev library. Because of unity's deep integration with multitouch gestures, it disallows many other systems from implementing basic gestures that are missing from the default multitouch gestures. This script will not override unity's gestures, but fill in some missing ones, working alongside unity's multitouch system.

Implemented gestures:

Two gesture options have been implemented for right click:

1 finger longpress * Standard operation is to open menu after finger is lifted. * Temporary workaround will bring up right click while still pressing
2 finger tap
Setting up script

To modify the delay for your right click, open the script in a text editor and modify the self.click_delay variable, the default is 0.5 seconds.

To install on a Raspberry Pi please follow the instructions below:

1) Install Dependencies:

    sudo apt-get install libts-bin evtest xinput python-dev python-pip

    then:

    sudo pip install pyuserinput

2) Change directory:

    cd /

3) Clone repository:

    sudo git clone https://github.com/HM-IHL/10.1-Touch-RPI.git

4) Change Directory:

    cd 10.1-Touch-RPI

5) Install python evdev:

    sudo python setup.py install

6) Change directory:

    cd Python_Touchscreen_Rightclick

7) Now you can run the software:

    sudo python Python_Touchscreen_RightClick.py

*Optional:
To make the code run at boot up, add to rc.local*

8) Edit rc.local:

    sudo nano /etc/rc.local

9) Add the following line before exit 0:

    sudo python /10.1-Touch-RPI/Python_Touchscreen_Rightclick/Python_Touchscreen_RightClick.py

10) Reboot the Pi:

    sudo reboot
