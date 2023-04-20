# BB65 Build Guide
A completely normal BlackPill-powered 65% DIY kit.

It can do almost anything you can think of between touchpad and steno.

![Finished Build](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/finished.png?raw=true "Finished Build")

# Table of Contents
- [Required Tools and Components](#user-content-required)
- [Recommended Tools](#user-content-recommended)
- [Kit Contents](#user-content-contents)
- [Step 0: Test and Flash Your BlackPill](#user-content-step0)
- [Step 1: Diodes](#user-content-step1)
- [Step 2: BlackPill](#user-content-step2)
- [Step 3: Standoffs](#user-content-step3)
- [Step 4: Encoder](#user-content-step4)
- [Step 5: Solder your switches](#user-content-step5)
- [Step 6: Acrylic Guard](#user-content-step6)
- [Step 7: Bottom Plate](#user-content-step7)
- [Step 8: Feet](#user-content-step8)


<a id="required">
 
# Required Tools

These tools and components are required to complete the project and are not included in the kit. The linked names of the components will generally link to a place where you can buy them.

- [Soldering Iron](https://www.amazon.com/s?k=soldering+iron)
    - Preferably a medium or small tip to make soldering the components easier.
- [Solder Wire](https://www.amazon.com/s?k=solder+wire+63%2F37+rosin+core)
    - I recommend a thinner 63/37 rosin core solder wire. In this build I am using [Kester Solder 63/37 .015 Dia](https://www.amazon.com/gp/product/B004X4L076).
- [Flush Cutters](https://mechwild.com/product/flush-cutters/)
- [Small Phillips Head Screwdriver](https://www.amazon.com/s?k=screwdriver+kit)
 
 
<a id="recommended">
 
# Recommended Tools

These tools are not necessary to complete the build, but might make the process a little easier for you or help you correct mistakes if you make them.

- Through-Hole leg bender forming tool
- Solder Sucker
- Solder Wick
- [Switch Puller](https://mechwild.com/product/switch-puller/)

<a id="contents">

# Kit Contents

Note: You might have extras of some components. This is normal and is to account for small mistakes.

### The Big Stuff
- PCB

![PCB](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/pcb.png?raw=true "PCB")

- Bottom

![Bottom](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/bottom.png?raw=true "Bottom")

- Plates

![Plates](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/plate.png?raw=true "Plates")


### Components

- BlackPill

![BlackPill](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/blackpill.png?raw=true "BlackPill")

- 70x Diodes

![Diodes](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/diodes.png?raw=true "Diodes")

- Encoder

![Encoder](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/encoder.png?raw=true "Encoder")

- Knob

![Knob](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/knob.png?raw=true "Knob")


### Assembly Hardware

- 1x Acrylic Guard

![Acrylic Guard](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/acrylic.png?raw=true "Acrylic Guard")

- 2x M2 12mm standoffs

![M2 12mm standoffs](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/12mm.png?raw=true "M2 12mm standoffs")

- 2x M2 8mm male female standoffs

![M2 8mm male female standoffs](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/8mm_m_f.png?raw=true "M2 8mm male female standoffs")

- 7x M2 8mm standoffs

![M2 8mm standoffs](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/8mm.png?raw=true "M2 8mm standoffs")

- 2x M2 6mm screws

![M2 6mm screws](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/6mm_screws.png?raw=true "M2 6mm screws")

- 14x M2 4mm screws

![M2 4mm screws](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/4mm_screws.png?raw=true "M2 4mm screws")

- 4x Rubber bumpons (feet)

![Rubber bumpons](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/parts/bumpons.png?raw=true "Rubber bumpons")



<a id="step0">

# Step 0: Test and Flash Your BlackPill

Firmware is on our firmware repo, available here:
[https://github.com/MechWild/mw_firmware/releases](https://github.com/MechWild/mw_firmware/releases)

All BlackPills that we sell are tested and preflashed with a modified version of either the BBS firmware or OBE firmware. This is just so that you can plug it in and test to make sure it is connected to your computer correctly and then flash it before building the rest of the board. By default, the blue light on the front of the black pill will be connected to the Num Lock status indicator for your computer. Plug in the black pill, and toggle Num Lock with another keyboard to see if the light responds accordingly. 
All BlackPills that we sell are tested and preflashed with a modified version of either the BBS firmware or OBE firmware. This is just so that you can plug it in and test to make sure it is connected to your computer correctly and then flash it before building the rest of the board. By default, the blue light on the front of the black pill will be connected to the Num Lock status indicator for your computer. Plug in the black pill, and toggle Num Lock with another keyboard to see if the light responds accordingly. 

Next, we will try and put it into bootloader mode. To do this, hold the button labeled “Boot0” on the top of the Blackpill, and while you are still holding that button, tap and release the “NRST” button. Then after a second or two, release the “Boot0” button. If nothing happens in QMK toolbox or if it still is responding when you push the Num Lock, then you should try again, because it didn’t go into bootloader mode.

Now we will try and flash the Blackpill using QMK toolbox (or your tool of choice.) Grab the appropriate firmware from the link at the beginning of this step, download it, select it in QMK Toolbox, put the BlackPill in bootloader mode then click flash.

<a id="step1">

# Step 1: Diodes

An easy but time consuming step. The direction of each diode matters and the black line on the diode should match up with the black line (or white line on black PCBs) on the silkscreen on the PCB. Make sure each diode is on the bottom of the PCB.

![Step 1: Diodes](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/1-0.png?raw=true "Step 1: Diodes")

![Step 1: Diodes](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/1-1.png?raw=true "Step 1: Diodes")

Solder them in place, clip the excess legs with your flush cutters, then flip it back to the front of the board and admire your handiwork.

<a id="step2">

# Step 2: Blackpill

Now we put the BlackPill on the board. It goes on the TOP of the PCB and has the components face outwards (UP) so that you can see all the cool parts and use the buttons on it if you need to after it is soldered in place. USB port goes towards the top of the board, so it can be accessed. In this guide, I am using a PillBug and sockets so the board is wireless

![Step 2: BlackPill](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/2-0.png?raw=true "Step 2: BlackPill")

<a id="step3">

# Step 3: Standoffs

Put the shorter standoffs that have a screw tip on one side (the 8mm male female standoffs shown in the contents above) in from the bottom on the two holes near the blackpill and then screw one of the 12mm standoffs onto the screw part so it looks like this:

![Step 3: Standoffs](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/3-0.png?raw=true "Step 3: Standoffs")

![Step 3: Standoffs](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/3-1.png?raw=true "Step 3: Standoffs")

![Step 3: Standoffs](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/3-2.png?raw=true "Step 3: Standoffs")

Then, for the rest of the holes around the perimeter of the board, you are going to put the short screws in from the top, and screw the 8mm standoffs onto the bottom side.

![Step 3: Standoffs](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/3-3.png?raw=true "Step 3: Standoffs")

![Step 3: Standoffs](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/3-4.png?raw=true "Step 3: Standoffs")

<a id="step4">

# Step 4: Encoder

If you're using one, this is the easiest time to put your encoder on.

![Step 4: LED Resistors](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/4-0.png?raw=true "Step 4: LED Resistors")

![Step 4: LED Resistors](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/4-1.png?raw=true "Step 4: LED Resistors")

<a id="step5">

# Step 5: Solder your switches

I will not be soldering switches in this guide, but now is the time to do it.

Please make sure to test before this step, because fixing things is WAY easier before it is fully assembled.

NOTE: IF YOU ARE USING THE PLATE, THE SWITCHES WILL NEED TO BE INSERTED THROUGH THE PLATE BEFORE BEING SOLDERED.

Also please make sure to put your stabilizers on BEFORE you start soldering switches on.

![Step 5: Solder your switches](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/5-0.png?raw=true "Step 5: Solder your switches")


<a id="step6">

# Step 6: Acrylic Guard

Next up, let's put the acrylic guard on. Peel the protective film off the acrylic (the blue film should be removed before assembly). Three of the corners are rounded, one is sharp. The sharp corner goes to the bottom left of the BlackPill area. Use the longer screws to attach it to the standoffs. It will look like this when you are done:

![Step 6: Acrylic Guard](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/6-0.png?raw=true "Step 6: Acrylic Guard")

<a id="step7">

# Step 7: Bottom Plate

Simple step. Attach the bottom plate using more of the short screws. The plate only lines up one way. 

![Step 7: Bottom Plate](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/7-0.png?raw=true "Step 7: Bottom Plate")

<a id="step8">

# Step 8: Feet

Somehow an even easier step than the last one. Put the little rubber feetsies onto the bottom plate.

![Step 8: Feet](https://github.com/MechWild/build_guides/blob/bb65/keyboards/bb65/pictures/steps/8-0.png?raw=true "Step 8: Feet")
