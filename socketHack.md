---
layout: default
title: Hacking Bluetooth Socket Instructions
nav_order: 11
---

# Instructions for hacking into the (optional) Bluetooth socket

## This instructions on how to connect the Bluetooth sockets into Home Assistant, you'll need to look up that information on the [Home Assistant forums](https://community.home-assistant.io/).

## This section assumes you're a tech wizard of some level, and that you have the ASC Bluetooth plug (which is optional when you made your purchase). If you have a Bluetooth device scanner then you can skip to the bottom to look at the possible commands you can send to the socket.

**- First, plug in your ASC Bluetooth socket. Make sure the LED is flashing blue, as that means it's waiting to pair.**

- If you don't have a Bluetooth scanner, download "nRF Connect" by Nordic Semiconductor for your Windows, Android, or Apple device.
  
<img src="images/BLEhack_1_nrfApp.jpg" width="600">

-  Use the Scan button at the top to search for the Bluetooth socket, and find the Bluetooth device that starts with "TramTek" and tap connect.

<img src="images/BLEhack_2_scan.jpg" width="600">

- Tap on the "Unknown Service", and the up-arrow on the "Unknown Characteristic" that has the "NOTIFY, WRITE" properties (the UUID number are at the bottom of this page).

<img src="images/BLEhack_3_send.jpg" width="600">

- Pick "TEXT (UTF-8)" from the drop down, and then send any one of these commands:

<img src="images/BLEhack_4_command.jpg" width="600">

## THE POSSIBLE COMMANDS YOU CAN SEND TO THE BLUETOOTH SOCKET:
All commands are UTF-8 text, do not put the "" around the UTF-8 Text: 
**"1,0" - On, infinite time**
**"0,0" - Off, infinite time**
**"1,x" - On, then a timer of x milliseconds (e.g. 1,5000 for On command sent immediately, then wait 5s, then turn off)**
**"0,x" - Off, then a timer of x milliseconds (e.g. 0,5000 for Off command sent immediately, then wait 5s, then turn on)**

**The UUID Service #: 4faf01c2-1b91-45e9-8fcc-c59cc333914b**
**The UUID characteristic #: af01c21b-9145-e98f-c5cc-9cc31c913a8b**

