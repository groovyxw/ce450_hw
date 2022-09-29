# Raspberry Pi 4 B Board Setup
# 1.	Preparation
Raspberry Pi 4 B Board
USB-C power supply
Micro SD card with Reader/Adapter (64 GB is preferred)
Monitor with micro-HDMI to HDMI cable, Keyboard, Mouse (Used once, only for the first-time setup)
Ethernet Cable (Optional, we can choose that connect/login to the board in wireless mode, e.g. WIFI)

 
# 2.	Set Up
## 1>	Install Raspberry Pi OS using Raspberry Pi Imager on your PC/laptop
### a.	Download Raspberry Pi Imager using this link Raspberry Pi OS – Raspberry Pi
### b.	Install Raspberry Pi Imager
### c.	Insert SD card in your PC/laptop and run Raspberry Pi Imager
Choose OS – “Raspberry Pi OS (32-bit)”
Choose Storage
Then Click Write
               
After the above steps are done, you have downloaded the OS into your SD Card successfully.
Reference Link: Projects | Computer coding for kids and teens | Raspberry Pi
## 2>	Setup the Raspberry Pi Board
### a.	Insert your SD card into Raspberry Pi Board
### b.	Connect Monitor, Keyboard and Mouse with your Raspberry Pi Board
### c.	Plug in Power Supply and Power On
After power on, you should see the power led is on.
 

### d.	In the monitor, follow the instructions to do basic configuration 
(Snapshots attached for reference) 
 
Remember the username and password that are used for logging into your raspberry pi board later.

So far, you have done the basic setup for the board already!!!!


### e.	Get the IP information of your Raspberry Pi Board 
Open a terminal, type command “ifconfig” (See the snapshots)
  
Now you have got the IP information.
Note: If you want to connect Raspberry Pi Board with Ethernet cable, use eth0 ip address information; otherwise, if you want to connect Raspberry Pi board in WIFI mode, use wlan0 ip address information.




### f.	Enable SSH and VNC interfaces, otherwise, you could not log in the board by PuTTY/VNC Viewer in next Step. (Snapshots are attached below)
 
 
 



### g.	Back to your PC/laptop, Download and Install Tool PuTTy or VNC Viewer
From this link Download VNC Viewer | VNC® Connect (realvnc.com) to download VNC Viewer.




### h.	If your vnc display normally, skip this step. Fix VNC display Issue in case you get the same problem with me in step g.

Problem: VNC ONLY display the top left corner of Raspberry Pi GUI in VNC terminal. At the same time, the display resolution is too low.
 


Fix: Change the boot configuration setting by modifying the file /boot/config.txt like this.
Login the board by putty and open a terminal.

$sudo vi /boot/config/txt
 

Edit file config.txt
  

$sudo reboot
 

After reboot, VNC Display normally:

 

Reference link: Fix :: Tiny VNC Display Rapsberry Pi Bullseye Upper Left Corner - YouTube



Done!!! 
