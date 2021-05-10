# BOP-Keyboard

BOP stands for Big Ortho Project, a 6 row by 20 column ortholinear keyboard running off of the Teensy++2.0 Controller.

## Jump to...
* [What's included](#included-in-the-box)
* [Build Guide](#build-guide)
  
## REPO Contents:
* Plate File in `.dxf` format, perfect for creating a 3D printed case from.
* Various Pictures of the Prototype boards, also shown below.
* QMK Hex and firmware coming soontm

### Pictures

![Image of BOP](https://i.imgur.com/mEWmMgv.jpg)
![Image of BOP](https://i.imgur.com/DbjVdvV.jpg)
![Image of BOP](https://i.imgur.com/IlWnuaP.jpg)


# Included in the Box:
#### Diodes - About 130x (120 needed)
![Image of Diodes](https://i.imgur.com/OT6Wkdf.jpg)
#### Standoffs + Screws - M3 Size (10x Standoffs and 20x Screws)
![Image of Standoffs](https://i.imgur.com/Eq6nieW.jpg)
#### Controller Headers - 2x 20 pin male and female headers
![Image of Headers](https://i.imgur.com/3377Pvh.jpg)
#### Stabilizers - 3x 2u Stabilizers
![Image of Stabilizers](https://i.imgur.com/qYNdEll.jpg)
#### Rubber Feet - 8x Feet
![Image of Feet](https://i.imgur.com/31zdTMb.jpg)
#### Controller - 1x Teensy++2.0 Micro Controller



# Build Guide:

### Step 1: Diodes
#### Estimated Time: 2-3 hours
[This is a really good video on how to solder smd diodes](https://youtu.be/Jpj3tilIaik?t=187). I recommend you watch this before soldering.
Start by orienting the PCB so that you can read "Design by Fruitykeeb" straight on. Next, place a small amound of solder the pad opposite to the "K" on each of the diode locations. There are 120 to do.
![Image of half pad](https://i.imgur.com/cNkuTjS.jpg)

Next, using tweezers or something similar, grab one diode and heat the bit of solder you just placed. Once the solder starts to melt, slide the diode into position. **Make sure the line on the diode is facing the "K" on the footprint. If it is not, key presses will not register!**
![Image of diode on](https://i.imgur.com/Bpd6NBi.jpg)

Finish the diodes by adding solder to the other pad. 

### Step 2: Headers
#### Estimated Time: 5-15 minutes
Keeping on the same side as the diodes, set the female headers onto the pcb. Making sure they are straight vertically, use tape to hold them in place. 
![Image of headers](https://i.imgur.com/nZECr6v.jpg)

Flip the pcb over and solder the headers in place. **Make sure there are no shorts between pins.**

Next, place the male headers onto the controller. The USB port should be facing up, leave the longer legs up as well. Using tape to hold them im place, flip the controller over and solder them in. Again, make sure there are no shorts between pins. Press the controller in to test fit, but remove for flashing and switches.
![Image of controller](https://i.imgur.com/E2dh0vQ.jpg)

### Step 3: Flashing the controller
#### Estimated Time: 5 minutes
My using [QMK Toolbox](https://github.com/qmk/qmk_toolbox), Open the default hex in the /keymaps/hex folder of this repo. 
In the MCU dropdown, select the `at90usb1286` option. Plug in the Teensy++2.0 and press the reset button at the bottom, then click `Flash` in the toolbox, this will flash the controller to the keymap you specify.

Press the controller in and using Via and tweezers, bridge the contacts where the switches would be to test each key. 
> If there is an issue where the last column spams the keys, there is a workaround detailed at the end.

### Step 4: Switches
#### Estimate Time: 45 mins - 1 hour.
Start by pressing some switches into the plate. I recommend switches placed as in the picture below, but use enough so the plate doesn't fall down.
![Image of plate with switches]()
