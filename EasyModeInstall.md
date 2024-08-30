---
layout: default
title: Easy Mode Installation
nav_order: 3
---

# Loading ESPHome on the TrampleTek Blue mat using [ESP Web tools](https://esphome.github.io/esp-web-tools/)

## These instructions are for default Home Assistant UI with the ESPHome add-on
If you are a Home Assistant power-user I suggest jumping to [Loading ESPHome on the TrampleTek mat](https://ascmats.github.io/mat_install.html) section and altering the directions and files as you need. If you are not a Home Assistant power-user yet, then these instructions are for you.

## (Warning) Easy Mode installation is dependent on web-based tools that might change, if they don't work jump to the [Loading ESPHome on the TrampleTek mat](https://ascmats.github.io/mat_install.html) section

## These are the step-by-step instructions

- First, open another window instance for your browser (must be Google Chrome or Microsoft Edge), as it can be hard to read the instructions and do use the ESP Web Tool (it covers the webpage).

- Click the button labeled "Connect" right below this line to start the ESP Web Tool:
<esp-web-install-button manifest="https://raw.githubusercontent.com/ASCKing9/TrampleTek-Blue-code/main/TrampleTekBlue.json" install-supported="">
        <i slot="unsupported">
          The option is not available because your browser does not support Web
          Serial. Open this page in Google Chrome or Microsoft Edge instead<span class="not-supported-i hidden">
            (but not on your iOS device)</span>.
        </i>
</esp-web-install-button>

- This pop-up will appear asking to select the COM port for your mat. You can plug and un-plug your mat's USB cable into the computer you're using to see which COM port appears and disappears, pick that option and press "connect." (If you don't see anything showing up when you plug your USB cable into the computer you may have a USB driver issue, if you hit cancel a pop-up will give you some info on hope to install the right USB drivers.

<img src="images/USBWeb_1_USBdialogConnect.png" width="400"> 

My COM port was COM9 in this example.

- If the ESP Web Tools succesfully connect to the device you will see this pop-up, click "Install TrampleTek Blue Firmware"

<img src="images/USBWeb_2_InstallFirmware.png" width="400"> 

- You will get another pop-up to confirm, click "Install"

<img src="images/USBWeb_3_InstallFirmwareConfirm.png" width="400"> 

- At first it will say "Erasing" for a bit, and then it will start to install

<img src="images/USBWeb_4_WaitingToInstall.png" width="400">

- After a few minutes it should be successful!

<img src="images/USBWeb_5_InstallDone.png" width="400"> 

- Next it should ask for you Wi-Fi credentials, if you make a mistake it'll let you know.

<img src="images/USBWeb_6_ConfigWifi.png" width="400">

- Once your Wi-Fi has been accepted you will see this. 







<img src="images/USBWeb_3_InstallFirmwareConfirm.png" width="600"> 
<img src="images/USBWeb_3_InstallFirmwareConfirm.png" width="600"> 
<img src="images/USBWeb_3_InstallFirmwareConfirm.png" width="600"> 
<img src="images/USBWeb_3_InstallFirmwareConfirm.png" width="600"> 
<img src="images/USBWeb_3_InstallFirmwareConfirm.png" width="600"> 
<img src="images/USBWeb_3_InstallFirmwareConfirm.png" width="600"> 
<img src="images/USBWeb_3_InstallFirmwareConfirm.png" width="600"> 




- This pop-up will appear asking to select the COM port for your mat. You can plug and un-plug your mat's USB cable into the computer you're using to see which COM port appears and disappears, pick that option and press "connect." (If you don't see anything showing up when you plug your USB cable into the computer you may have a USB driver issue, if you hit cancel a pop-up will give you some info on hope to install the right USB drivers.

<img src="images/USBWeb_1_USBdialogConnect.png" width="600"> 
My COM port was COM9 in this example.

- If the ESP Web Tools succesfully connect to the device you will see this pop-up

- sdf






## Ignore this section, active testing happening

<script
  type="module"
  src="https://unpkg.com/esp-web-tools@10/dist/web/install-button.js?module"
></script>

<esp-web-install-button manifest="https://raw.githubusercontent.com/ASCKing9/TrampleTek-Blue-code/main/TrampleTekBlue.json" install-supported="">
        <i slot="unsupported">
          The option is not available because your browser does not support Web
          Serial. Open this page in Google Chrome or Microsoft Edge instead<span class="not-supported-i hidden">
            (but not on your iOS device)</span>.
        </i>
</esp-web-install-button>
