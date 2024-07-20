---
layout: default
title: Using TrampleTek in HA
nav_order: 7
---

# Explanation of the User Interface (UI) elements of the TrampleTek Blue (Home Assistant version)

## User Interface Overview

<img src="images/HA_UI_overview.png" width="600">

The UI is seperated into four visible components "Calibration", "Dropdown Sensitivity", "Sensitivity", and "Mat Sensor" and one secret component (not pictured here) for power users "Pressure voltage". 

Your UI elements may show up in a different order, and I will explain them from simpliest to most complex.

### Mat Sensor monitor

<img src="images/HA_UI_binary.png" width="600">

This component is as simple as it gets, it just shows when the mat has been triggered to on or off. This is most likely the entity you will use to trigger your HA automations.

### Dropdown Sensitivity

<img src="images/HA_UI_dropdown.png" width="600">

This component sets the sensitivity of the mat from a drop down menu. The five options are long to help explain them in the UI, the options are:

**1) Low weight object (<1 lb) on an uncovered mat, or a heavy weight object on a heavy weight covered mat (e.g. adult human with mat under mattress). Very sensitive, may cause false triggering**

- This option makes the mat very sensitive, so sensitive that it may trigger when it imagines something on it. This setting is not recommended unless you are trying to use it as a bed occupancy monitor.

**2) Low weight object (~1 lb) on an uncovered mat, or a heavy weight object on a medium weight covered mat (e.g. adult human with mat under rug)**

- This option is great for making sure your mat triggers for light packages or animals, it is the recommended default setting for high sensitivity with very few mistakes.

**3) Medium weight object (~1-20 lb) on an uncovered mat, or a heavy weight object on a light weight covered mat (e.g. adult human with mat under light rug)**

- This option is for triggering the mat with sizable objects, it may still trigger for small animal and packages, but if you put the mat under a cushion or rug then it will take a grown adult amount of weight to trigger the mat.

**4) Heavy weight object (>20 lb) on an uncovered mat, not likely to work well if mat is covered**

- This option is for triggering the mat only with heavy objects, this will likely never trigger for small or medium sided animals or packages. This is a great option if you want to use the mat to detect a car tire.

**5) Custom**

- This means you've selected a custom sensitivity from the "Sensitivity" slider (which is the next UI element!).







## (TO DO) Each part of the UI elements will explained with details, examples, and ways to use each element. Is the UI is still being finalized I have not written this section fully yet.


<img src="images/mat_usage_image.png" width="600">

This documentation will help you through the hardware setup for through Home Assistant and through some troubleshooting if things don't go quite as smoothly as expected.

You can alway contact me at Raymond@asc.com if you have issues, questions, or suggestions for the documentation.

Let's get started by checking to make sure you have the [Requirements](https://ascmats.github.io/requirements.html) ready to set up TrampleTek Blue (Home Assistant version).
