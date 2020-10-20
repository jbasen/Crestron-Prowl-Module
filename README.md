# Crestron-Prowl-Module
This module pushes notifications to your iPhone, iPod Touch, and iPad through Prowl.  

This module consists of the core S# module Prowl.clz, a Simpl+ wrapper Prowl v1.0.usp/Prowl v1.0.ush, 
and this help file - Module Prowl v1.0 Help.pdf. All 4 of these should simply be placed in your Crestron 
Usrsplus directory.  

An example program, Prowl Module Demo.smw is provided to further show how the module can be used.  
Licensing

The Prowl notifications module, PushOver notifications module, and Vybit notifications module all provides the 
ability for a Crestron program to send push notifications to a homeowner’s smart phone and/or tablet.   
With these modules you can, for example:

1.	Send a notification to a smart phone when the burglar alarm is tripped.  
2.	Send a notification to a smart phone when the temperature in the house gets too cold and there is risk of a pipe freezing.

There are minor differences in functionality between the three modules that may make one a better fit for a specific client 
than the others.

The modules are all written in Simpl# and each has an example program demonstrating its use as well as detailed help files.

This family of modules is released as shareware.  As a developer the modules are free for use on your own personal Crestron 
system.  Dealers are also invited to use them in their showrooms.  However, if you decide to use any, or all of them, on 
customer systems where you, or the dealer/csp you work for will profit from them than I ask for a single payment of $100.  

What you get is 

1) My thanks
2) Permission to use Prowl module, PushOver module, and Vybit module on as many client projects as you want
3) A copy of the Simpl# source code for each module (only a binary executable is included with each example program)
4) Good Karma

You can contact me at jay.m.basen@gmail.com to arrange for payment.

Thanks - Jay Basen

Module Help

Digital Inputs
Signal	    Description
Initialize  Pulse to initialize the module before use
Send        Pulse after all serial inputs have been populated to push the notification to Prowl

Analog Inputs
None

Serial Inputs
Signal	    Description
Api_key1$	  Personal API Key provided by the web site www.prowlapp.com.  This key uniquely identifies the recipient of notifications.  
Api_key2$	  Personal API Key provided by the web site www.prowlapp.com.  This key uniquely identifies the recipient of notifications.
Api_key3$	  Personal API Key provided by the web site www.prowlapp.com.  This key uniquely identifies the recipient of notifications.
Api_key4$	  Personal API Key provided by the web site www.prowlapp.com.  This key uniquely identifies the recipient of notifications.
Api_key5$	  Personal API Key provided by the web site www.prowlapp.com.  This key uniquely identifies the recipient of notifications.
Priority$	  Default value of "0" if not provided. A value ranging from "-2" to "2" representing the priority as follows:
"-2"	- 	  Very Low
"-1"	- 	  Moderate
"0"		- 	  Normal
"1"		- 	  High
"2"		- 	  Very High
Url$	      The url of the application that will be opened when the notification is received by the iOS device.  For example, 
            "crestron-app://" will launch the Crestron App.  You can also setup redirections in the Prowl iOS app to open apps 
            based on receiving a specific notification.  If that is done then "" should be sent to this input.
Application$  The name of your application or the application generating the event.  For example, "Crestron".
Event$	      The name of the event or the subject of the notification.  For example, "Burglar Alarm".
Description$  A description of the event, generally terse.  For example, "The Burglar Alarm has been tripped".

Digital Outputs
None

Analog Outputs
None

Serial Outputs
None

Parameters
None

Steps for Configuring www.prowlapp.com to Distribute Notifications to your iOS devices and Setup of your iOS Devices to Receive 
Notifications

The Prowl Crestron module requires the following to push notifications to your iOS devices:

1.	A free account needs to be created on www.prowlapp.com
2.	An API Key needs to be created while logged into www.prowlapp.com
3.	The API Key needs to be added to the Crestron program so it is sent to the Prowl module.
4.	The iOS App "Prowl: Easy Push Notifications" by Zachary West needs to be installed on the iOS devices where you wish 
    to receive notifications.  You must then login to the app using the same username/password that you created for 
    www.prowlapp.com.  NOTE - There is a small fee for this app.

