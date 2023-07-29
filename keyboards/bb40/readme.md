# BB40 Build Guide
A completely normal BlackPill-powered DIY 40% kit.

![Finished Build](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/finished.png?raw=true "Finished Build")

# Table of Contents
- [Required Tools and Components](#user-content-required)
- [Recommended Tools](#user-content-recommended)
- [Kit Contents](#user-content-contents)
- [Step 0: Test and Flash Your BlackPill](#user-content-step0)
- [Step 1: Diodes](#user-content-step1)
- [Step 2: Resistors](#user-content-step2)
- [Step 3: BlackPill/PillBug](#user-content-step3)
- [Step 4: Status LEDs](#user-content-step4)
- [Step 5: Encoder](#user-content-step5)
- [Step 6: Testing Time](#user-content-step6)
- [Step 7: Stabs/Switches](#user-content-step7)
- [Step 8: Standoffs](#user-content-step8)
- [Step 9: Bottom and Feet](#user-content-step9)
- [Step 10: Acrylic Guard](#user-content-step10)
- [Step 11: Keycaps and Submit For Inspection](#user-content-step11)


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

![PCB](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/pcb.png?raw=true "PCB")

- Bottom

![Bottom](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/bottom.png?raw=true "Bottom")

- Plate

![Plate](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/plate.png?raw=true "Plate")


### Components

- BlackPill

![BlackPill](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/blackpill.png?raw=true "BlackPill")

- 45x Diodes

![Diodes](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/diodes.png?raw=true "Diodes")

- Encoder

![Encoder](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/encoder.png?raw=true "Encoder")

- Knob

![Knob](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/knob.png?raw=true "Knob")


### Assembly Hardware

- Acrylic Guard

![Acrylic Guard](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/acrylic.png?raw=true "Acrylic Guard")

- 2x M2 10mm female-female standoffs

![M2 10mm standoffs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/10mm.png?raw=true "M2 10mm standoffs")

- 2x M2 8mm male-female standoffs

![M2 8mm male female standoffs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/8mm_m_f.png?raw=true "M2 8mm male female standoffs")

- 4x M2 8mm female-female standoffs

![M2 8mm standoffs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/8mm.png?raw=true "M2 8mm standoffs")

- 2x M2 6mm screws

![M2 6mm screws](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/6mm_screws.png?raw=true "M2 6mm screws")

- 10x M2 4mm screws

![M2 4mm screws](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/4mm_screws.png?raw=true "M2 4mm screws")

- 4x Rubber bumpons (feet)

![Rubber bumpons](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/parts/bumpons.png?raw=true "Rubber bumpons")



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

The orientation of the diode matters! Black line on the diode should line up with the line on the silkscreen drawing underneath it. Diodes go on the bottom of the PCB (the side opposite the side where the switches go in).

![Step 1: Diodes](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/1-0.png?raw=true "Step 1: Diodes")

![Step 1: Diodes](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/1-1.png?raw=true "Step 1: Diodes")

<a id="step2">

# Step 2: Resistors

Orientation of the resistors doesn't matter here. Just make sure they are in the right spot, and it will probably look better if they are all facing the same direction.

![Step 2: Resistors](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/2-0.png?raw=true "Step 2: Resistors")

![Step 2: Resistors](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/2-1.png?raw=true "Step 2: Resistors")

<a id="step3">

# Step 3: BlackPill/PillBug

Put on the BlackPill or PillBug (your choice, I socketed here like I normally do since I test a ton of stuff.)

Components face upwards with the USB port facing to the top right corner of the keyboard.

![Step 3: BlackPill/PillBug](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/3-0.png?raw=true "Step 3: BlackPill/PillBug")

![Step 3: BlackPill/PillBug](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/3-1.png?raw=true "Step 3: BlackPill/PillBug")

<a id="step4">

# Step 4: Status LEDs

Status LEDs now! The easy way to tell which is which is that the long leg of the LED goes in the hole closest to the edge of the board. The pictures below highlight which is which. No real order specifically required, but when I do 3 color status LEDs like this, I like to do Red, Green, Blue from the top. 

![Step 4: Status LEDs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/4-0.png?raw=true "Step 4: Status LEDs")

![Step 4: Status LEDs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/4-1.png?raw=true "Step 4: Status LEDs")

<a id="step5">

# Step 5: Encoder

Now is the time to put on the encoder if you are using one. I put one in for the picture, but removed it for my personal build I am doing in this guide, so don't be confused if it isn't shown again.

![Step 5: Encoder](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/5-0.png?raw=true "Step 5: Encoder")

<a id="step6">

# Step 6: Testing Time

Now is the time to use your tweezers to test all the switch positions that you need. Doing it now before soldering switches makes it a billion times easier to troubleshoot if you get some weird results.

<a id="step7">

# Step 7: Stabs/Switches

Go ahead and put all the switches and stabilizers you are using on now. Importantly, you will want to make sure that you put your stabilizers on before soldering switches, and the switches go THROUGH the switchplate before being soldered as well.

![Step 7: Stabs/Switches](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/7-0.png?raw=true "Step 7: Stabs/Switches")

<a id="step8">

# Step 8: Standoffs

Simple step with lots of small parts. Start off with the two mount points for the acrylic guard. I find it easiest for these to hold them on one side and just screw the other side on with my other hand like shown in the pictures here. NOTE: The standoffs you are using on the top side where the acrylic mounts are going to be slightly longer than the others in the bag!

![Step 8: Standoffs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/8-0.png?raw=true "Step 8: Standoffs")

Then you will need to pass a screw through the plate with your screwdriver, and screw the standoffs on from the other side.

![Step 8: Standoffs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/8-1.png?raw=true "Step 8: Standoffs")

![Step 8: Standoffs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/8-2.png?raw=true "Step 8: Standoffs")

![Step 8: Standoffs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/8-3.png?raw=true "Step 8: Standoffs")

Do that for all the holes, so that when you flip it to look at the bottom (like this next pic) you will see 6 total standoffs to screw the bottom on with.

![Step 8: Standoffs](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/8-4.png?raw=true "Step 8: Standoffs")

<a id="step9">

# Step 9: Bottom and Feet

Put the bottom on and then the four rubber feet into the corners.

![Step 9: Bottom and Feet](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/9-0.png?raw=true "Step 9: Bottom and Feet")

<a id="step10">

# Step 10: Acrylic Guard

Install the acrylic guard now. If it has blue film on it (it probably does by default) then peel it off first.

![Step 10: Acrylic Guard](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/10-0.png?raw=true "Step 10: Acrylic Guard")

Guard on!

<a id="step11">

# Step 11: Keycaps and Submit For Inspection

All done! Put the keycaps on then have your cat check it over for approval. Enjoy!

![Step 11: Keycaps and Submit For Inspection](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/finished.png?raw=true "Step 11: Keycaps and Submit For Inspection")


Inspection time!

![Step 11: Keycaps and Submit For Inspection](https://github.com/MechWild/build_guides/blob/bb40/keyboards/bb40/pictures/steps/inspected.png?raw=true "Step 11: Keycaps and Submit For Inspection")