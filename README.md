# domo-ifttt

Provides a relatively quick and easy way to voice control multiple devices in Domoticz using just 2 applets in IFTTT.


Added control for GROUPS and SCENES!
=======
It controls all Light switches (all devices set as switch), Scene's and Groups. 
Support for devices like dimmers and reading value's from temp etc are on my tasklist.


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

## Changes:
- Added Group and Scene support.

- Optimised (faster) Domoticz Query

- Optional search favorite devices Only or ALL (can be set as option in top PHP file)

## Problems / Solutions:
### PHP file not working / Domoticz Offline message.
- Domoticz has no PHP support, install Apache or another webserver (advice: on the same device) and put this script in there.
Apache runs perfectly if installed on Raspberry with Domoticz besides it.
It will run fast and without delay.
Apache on Raspberry setup instructions: [klik here](https://www.raspberrypi.org/documentation/remote-access/web-server/apache.md) 

## About 
- I started Domoticz to link with IFTTT applets to use Google Home, but after adding 32 devices i stopped.

I found this script and forked this (Thnx DSwinton for the original!) and trying to improve it wherever i can.
Github is new for me, so bare with me when I try to merge, pull, push, etc...

Any comments? Please let me know what you think or like to be improved.
