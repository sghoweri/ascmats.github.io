---
layout: default
title: YAML Code Installation
nav_order: 6
---

# Instructions for installing the YAML code on to the TrampleTek mat

- At this point you have the is mat registered with Home Assistant(!) and it may prompt you that a new device was discovered. If you add the device now it won’t do anything, as it doesn’t have any ability to trigger any of your devices, that’s what the YAML code does. 

-	You can close your open ESPHome Web browser tab for now and get back to the ESPHome Open Web UI. (Main Home Assistant page -> settings-> add-on -> ESPHome -> Open Web UI). You may need to wait or refresh this screen a few times until your device shows up as “Online”
<img src="" width="600"> 

 


•	Click on “EDIT” to add your Wi-Fi settings and the firmware to run the mat!
<img src="" width="600"> 

 




•	This will open up the YAML code for your mat, and you should see this (I’m not worried about showing sensitive details here because I’ll be remaking this device with different values in the future):
<img src="" width="600"> 

 

•	VERY IMPORTANT, MAT MAY NOT WORK WITHOUT DOING THIS First we need to add this line in the Wi-Fi section: “output_power: 8.5dB” (details about why here). We have to do this because there is a possible issue with the ESP’s Wi-Fi and this helps to fix that issue. Click save.
<img src="" width="600"> 

 




•	Next you need to put in your Wi-Fi credentials. You can either put your details directly into this file (you must have double quotations around the SSID and the password) or use the secrets.yaml file (optional steps below). If you put in your details directly, click save.
<img src="" width="600"> 

 

o	(Optional, using secrets.yaml) Get to the Open Web UI view and click on “Secrets” in the top right corner. 
<img src="" width="600"> 

 





o	(Optional, using secrets.yaml) If this file is empty, follow the structure of the information in the image and put in your SSID and password inside the double quotations just like the made up Wi-Fi details below. Click Save!
<img src="" width="600"> 

 


•	Copy the code from YAML file at https://github.com/ASCKing9/TrampleTek-Blue-code/blob/main/TrampleTek_Threshold_Trigger_ESPHome.yaml, scroll down to the bottom of your YAML file and paste in the code. 
<img src="" width="600"> 
 

•	Save and upload:
 
•	You will be prompted with the install list, we will use “Plug into the computer” again. Follow the same steps we used previously to install the new YAML code onto the mat (the [your mat’s name].bin will have the same name).
<img src="" width="600"> 
 






•	 After you finish installing, you can close out of ESPHome Web tab and navigate back to the ESPHome Open Web UI and click on “LOGS”. (Main Home Assistant page -> settings-> add-on -> ESPHome -> Open Web UI).
<img src="" width="600"> 
 
•	 If everything was successful, you should see your Wi-Fi details in the log, along with a stream of data coming out of the mat. The mat is successfully connected and sending data to Home Assistant!
<img src="" width="600"> 
 
•	(NOTE: If you ever need to save and install any changes to the YAML code, you should be able to use the “Wirelessly” option moving forward. With the “output_power: 8.5dB” line your wireless connection should be stable enough to use this option.)
<img src="" width="600"> 









