---
layout: default
title: Installing the TrampleTek mat
nav_order: 4
---

# Installing the TrampleTek mat (~8 min, compile and upload speed can make it slower)

## If you're a Tech Wizard, these instructions are for default Home Assistant + ESPHome add-on instructions
If you are not using the ESPHome without the Home Assistant add-on (e.g. you're running Docker on a Linux machine), some of these instructions will need to altered for you. If you a tech wizard using Home Assistant in an advanced setup like Docker/Linux you may need to use the command line instructions for ESPHome [here](https://esphome.io/guides/getting_started_command_line.html).

## These are step-by-step instructions

- Open ESPHome in the Settings -> Add-ons section.
<img src="images/select_addons.png" width="600">

•	Open the Web UI.
<img src="images/select_open_web_UI.png" width="600">

•	Add a new device.
<img src="images/select_new_device.png" width="600">

•	Press Continue.
<img src="images/select_new_device_continue.png" width="600">
For right now we will use the ESPHome web interface eventually, but there are some things we need to setup to make sure the mat’s Wi-Fi is configured for Home Assistant.

•	Pick a name for your mat.
<img src="images/pick_a_name.png" width="600">
I find shorter is better for keeping the Home Assistant interface elements less crowded.

•	Pick ESP32-C3, that’s the micro-controller brain we’re using.
<img src="images/pick_ESP32_c3.png" width="600">

•	Your new device will show up in the background, and it will prompt you to pick an encryption key. Go ahead and press “Install” after you keep or change the encryption key.
<img src="images/install_device.png" width="600"> 

•	Plug the USB-C end of your cable into the mat and the USB into the computer your using, and pick “Plug into this computer.”
<img src="images/plug_in_this_computer.png" width="600"> 
Side note: I think the simplest option is actually “Plug into the computer running ESPHome Dashboard” (for me, the Raspberry Pi running Home Assistant), but not everyone has easy access to their Home Assistant device. I will not cover the instructions for that option here, but feel free to explore that option if you’re interested.

•	This step may take a 2-4 or more mins, and all you see if the spinning blue circle to let you know something is happening. It takes so long because it’s compiling the project from scratch and then downloading it.
<img src="images/download_project_wating.png" width="600"> 

•	Eventually option “1. Download project” will go blue to show it’s ready, click on it.
<img src="images/download_project_done.png" width="600"> 

•	A new pop up will show up, pick “Modern format.”
<img src="images/modern_format.png" width="600">  

•	Depending on your browser it may identify the [your device name].bin file as insecure or unknown, you may need to press “keep” or accept this unknown file. 
<img src="images/keep_bin_file.png" width="600"> 

•	Now we press the next step, “2. Open ESPHome Web.”
<img src="images/open_ESPHome_web.png" width="600">  

•	The ESPHome Web interface is not supported on all browsers (e.g. Safari), you will need Chrome or another browser that supports ESPHome Web. ESPHome Web will open a new tab on your browser, press “Connect” to start looking for the device:
<img src="images/ESPHome_web_connect.png" width="600"> 

•	This pop up will show up and you have need to figure out which device is your TrampleTek Mat, and what COM port it is on (mine was COM28 in this example). With the pop up window open you may be able to unplug and re-plug the USB cable in and see which COM port appears and disappears. This usually takes me a couple tries to figure out the COM port and make sure the device is “available” to the computer.
<img src="images/ESPHome_web_connect_usb.png" width="600"> 

•	Once you get the right COM port pick this option, to install the [your mat name].bin file you just download. 
<img src="images/ESPHome_web_connect_install.png" width="600"> 

•	This will open a new pop up, click “Choose file” and navigate to wherever you downloaded your [your device name].bin. Select the file and click open (the open button was cut off in the image below, it’s on the right).
<img src="images/ESPHome_web_connect_bin_browse.png" width="600"> 

•	Click Install. 
<img src="images/ESPHome_web_connect_bin_install.png" width="600"> 
WARNING: THIS STEP MIGHT FAIL! That’s okay, it just means the computer can’t (or made a mistake and didn’t) put the mat into “boot mode”. Sometimes you can disconnect and reconnect the mat (you will need to redo the previous step on connecting to the mat with ESPHome web) and then the install button will work. If you continue to get an error about “timing out” you will to manually put the mat into “boot mode”. 
<img src="" width="600"> 

 


•	OPTIONAL: These steps are IF NEEDED to put your mat in “boot mode” if the install step above repeatedly fails or times out.
<img src="" width="600"> 

o	Disconnect the USB-C cable and pop off the protective cover of the circuit board.
<img src="" width="600"> 

 

o	There is a long plastic clip on the front and back of the protective box keeping it snapped to the circuit board. It’s tight but pry up the front of the protective box to pop it off.
<img src="" width="600"> 

 







o	With the protective cover off plug the cable back in! You then must hold the “Boot” button (it is a small sideways button on the right) and while the “Boot” button is held down you must press and release the “Reset” button (the small sideways button on the left).
<img src="" width="600"> 

 

o	You will need to go back to the “Connect” step above after unplugging and re-plugging the device into the computer. Get back to this screen and install!
<img src="" width="600"> 

 

•	If this step fails try doing the “Boot and reset” sequence again, as the circuit board may not have made it to “boot mode”. 
<img src="" width="600"> 






•	If it the install step worked, you’ll start seeing loading:
<img src="" width="600"> 

 


•	When it’s done you’ll see this!
<img src="" width="600"> 

 









o	(OPTIONAL) If you had to manually put the mat into “boot mode,” unplug the USB-C cable and clip the protective cover back onto the circuit board. Make sure the USB-C connection hole in the protective cover is aligned with the cutout in the waterproofing plastic sheet before squeezing the protective to snap it back into place. Plug the USB-C cable back in.
<img src="" width="600"> 

 

















4.	Add YAML code
At this point you have the is mat registered with Home Assistant(!) and it may prompt you that a new device was discovered. If you add the device now it won’t do anything, as it doesn’t have any ability to trigger any of your devices, that’s what the YAML code does. 

•	You can close your open ESPHome Web browser tab for now and get back to the ESPHome Open Web UI. (Main Home Assistant page -> settings-> add-on -> ESPHome -> Open Web UI). You may need to wait or refresh this screen a few times until your device shows up as “Online”
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











## Next Steps

The firmware installed we can move onto to looking at what the mat can do! (link to next section).
