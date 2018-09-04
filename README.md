# domo-ifttt

Provides a relatively quick and easy way to voice control multiple devices in Domoticz using just 2 applets in IFTTT.

Added control for GROUPS and SCENES!

For now it only works with Domoticz Favorite devices. Soon also non favorite devices will be supported.

PHP Support:
Domoticz has NO php support, and all attempts I tried to enable this failed.
Easy solution is to install Apache webserver on same device as domoticz.
Step by Step Apache install on Raspberry: https://www.raspberrypi.org/documentation/remote-access/web-server/apache.md 
This worked perfectly for me, and on a Raspberry V3B it runs very fast with no delay at all.

## Instructions:
1. Make sure you have a webserver with PHP support (Domoticz has NO php support!)
2. Install this PHP file on a web server (prefered running on the same box as Domoticz).
3. Edit the values at the top of the file - password domoticz URL must be set
4. Forward a port to the (domoticz) web server
5. Give it a bit of a test with a URL like this...  https://yourserver.whatever/domo-ifttt.php?passkey=<Password_Set_in_Php_script>&devName=<Exact_Domoticz_Device_Name>&devState=1
6. Have a look in Syslog to see how it went
7. If it's working locally, it's time to set up IFTTT - check "README - IFTTT Setup.pdf" for instructions
8. Repeat IFTTT step by creating a 2nd applet but now with "Off" and devState=0
9. Have Fun

## About 
- I started Domoticz to link with IFTTT applets to use Google Home, but after adding 32 devices i stopped.

I found this script and forked this (Thnx DSwinton for the original!) and trying to improve it wherever i can.
Github is new for me, so bare with me when I try to merge, pull, push, etc...

Any comments? Please let me know what you think or like to be improved.
