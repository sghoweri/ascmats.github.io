---
layout: default
title: (BETA) Sleep mat code
nav_order: 12
---

# This is for testers of the TrampleTek Sleep (name still TBD) to install the sleep mat code

## If you would like to join the beta test please join the ASC Discord ([invite link](https://discord.gg/cB9P6NmYJg))

### This install assumes you're using the ESPHome add-on in Home Assistant
If you are a Home Assistant power-user I suggest jumping to [Loading ESPHome on the TrampleTek mat](https://ascmats.github.io/docs/Manual-Installation/mat_install.html) section and altering the directions and files as you need. If you are not a Home Assistant power-user yet, then these instructions are for you.

## (Warning) Easy Mode installation is dependent on web-based tools that might change. If this mode works, great(!), you can skip the Manual Install section. If this doesn't work jump to the [Manual Installation](https://ascmats.github.io/docs/Manual-Installation/) section.

## These are the step-by-step instructions

- ESP Web tools only work with Google Chrome or Microsoft Edge. Open another window of your browser, as it can be hard to read the instructions and use the ESP Web tool (it covers the webpage).

- Open a browser tab with the [Easy Model Installation](https://ascmats.github.io/EasyModeInstall.html) because you'll be using the "connect" button below and then following the Easy Mode Installation right at the "The below pop-up" step.

- Click the button labeled "Connect" right below this line to start the ESP Web tool:
<esp-web-install-button manifest="https://raw.githubusercontent.com/ASCKing9/TrampleTek-Blue-code/refs/heads/main/TrampleTek_Debug/SleepMatBeta/TrampleTek_Sleep.json" install-supported="">
        <i slot="unsupported">
          The option is not available because your browser does not support Web
          Serial. Open this page in Google Chrome or Microsoft Edge instead<span class="not-supported-i hidden">
            (but not on your iOS device)</span>.
        </i>
</esp-web-install-button>

- Now go to the [Easy Model Installation](https://ascmats.github.io/EasyModeInstall.html) page and follow the instructions there. You'll know you used the right button when you see the name - **"TrampleTek Sleep Firmware"**.

## Next Steps
If this worked, great! If not ask in the Discord for help, or email me directly at Raymond@asc.com.

Join the [ASC Discord server](https://discord.gg/cB9P6NmYJg) if you have questions or comments about this page.

<script
  type="module"
  src="https://unpkg.com/esp-web-tools@10/dist/web/install-button.js?module"
></script>
