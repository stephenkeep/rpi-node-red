#Node-RED on Raspberry Pi

Installing Node-RED on a Raspberry Pi Step One: Download Raspbian Jessie Lite: 

[https://www.raspberrypi.org/downloads/raspbian/](https://www.raspberrypi.org/downloads/raspbian/)

Step Two: Unzip the download:

    unzip 2016–02–26-raspbian-jessie-lite.zip

Step Three: Insert your SD card into your Mac and find the disk name

    diskutil list

Step Four: Once you have found the disk unmount it

    diskutil unmountdisk /dev/disk2

Step Five: Install the image on the SD card

    sudo dd if=2016–02–26-raspbian-jessie-lite.img of=/dev/rdisk2 bs=1m

Step Six: Unmount the SD Card

    diskutil unmountdisk /dev/disk2

Step Seven: Connect to the Pi via SSH, this can take some time to connect to the network first time.

    ssh pi@192.168.1.111

Step Eight: Enter the default password ‘raspberry’ when prompted.

##Install Node.js 

Download Node.js source Raspberry Pi Model A, B, B+ and Compute Module

```
wget https://nodejs.org/dist/v4.0.0/node-v4.0.0-linux-armv6l.tar.gz 
tar -xvf node-v4.0.0-linux-armv6l.tar.gz 
cd node-v4.0.0-linux-armv6l
```

   Copy to /usr/local

    sudo cp -R * /usr/local/

Node.js is properly install and you have the right version, run the command node -v

##Install Node-RED

    sudo npm install -g --unsafe-perm  node-red
