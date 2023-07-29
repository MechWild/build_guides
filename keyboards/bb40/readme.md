# BB40 Build Guide
A completely normal BlackPill-powered DIY 40% kit.

![Finished Build](https://github.com/MechWild/build_guides/blob/main/keyboards/bb40/pictures/steps/finished.png?raw=true "Finished Build")

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

![PCB](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/pcb.png?raw=true "PCB")

- Bottom

![Bottom](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/bottom.png?raw=true "Bottom")


### Components

- BlackPill

![BlackPill](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/blackpill.png?raw=true "BlackPill")

- 25x Diodes

![Diodes](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/diodes.png?raw=true "Diodes")

- Encoder

![Encoder](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/encoder.png?raw=true "Encoder")

- Knob

![Knob](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/knob.png?raw=true "Knob")

- Per-key SMD LEDs

![Per-key SMD LEDs](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/perkey_smd.png?raw=true "Knob")

- Underglow SMD LEDs

![Underglow SMD LEDs](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/underglow_smd.png?raw=true "Knob")


### Assembly Hardware

- Acrylic Guard Selection

![Acrylic Guards](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/acrylic.png?raw=true "Acrylic Guards")

- 2x M2 10mm female-female standoffs

![M2 10mm standoffs](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/10mm.png?raw=true "M2 10mm standoffs")

- 2x M2 8mm male-female standoffs

![M2 8mm male female standoffs](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/8mm_m_f.png?raw=true "M2 8mm male female standoffs")

- 7x M2 8mm female-female standoffs

![M2 8mm standoffs](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/8mm.png?raw=true "M2 8mm standoffs")

- 2x M2 6mm screws

![M2 6mm screws](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/6mm_screws.png?raw=true "M2 6mm screws")

- 14x M2 4mm screws

![M2 4mm screws](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/4mm_screws.png?raw=true "M2 4mm screws")

- 4x Rubber bumpons (feet)

![Rubber bumpons](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/parts/bumpons.png?raw=true "Rubber bumpons")



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

The orientation of the diode matters! Black line on the diode should line up with the line on the silkscreen drawing underneath it. Diodes go on the same side as the LEDs did, but are soldered on the other side.

![Step 1: Diodes](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/1-0.png?raw=true "Step 1: Diodes")

![Step 1: Diodes](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/1-1.png?raw=true "Step 1: Diodes")


<a id="step2">

# Step 2: Resistors

words here

![Step 2: Resistors](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/2-0.png?raw=true "Step 2: Resistors")

![Step 2: Resistors](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/2-1.png?raw=true "Step 2: Resistors")


<a id="step3">

# Step 3: BlackPill/PillBug

Put on the BlackPill or PillBug (your choice, I socketed here like I normally do since I test a ton of stuff.)

Components face upwards with the USB port facing to the top right corner of the keyboard.

![Step 3: BlackPill/PillBug](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/3-0.png?raw=true "Step 3: BlackPill/PillBug")


<a id="step4">

# Step 4: Status LEDs

words here

![Step 4: Status LEDs](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/4-0.png?raw=true "Step 4: Status LEDs")


<a id="step5">

# Step 5: Encoder

Now is the time to put on the encoder if you are using one.

![Step 5: Encoder](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/5-0.png?raw=true "Step 5: Encoder")


<a id="step6">

# Step 6: Testing Time

Now is the best time to test all the LEDs and encoder functionality. It is also a good time to use your tweezers to test all the switch positions that you need.

![Step 6: Testing Time](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/6-0.png?raw=true "Step 6: Testing Time")


<a id="step7">

# Step 7: Stabs/Switches

Go ahead and put all the switches and stabilizers you are using on now. Importantly, you will want to make sure that you put your stabilizers on before soldering switches, and the switches go THROUGH the switchplate before being soldered as well.

![Step 7: Stabs/Switches](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/7-0.png?raw=true "Step 7: Stabs/Switches")


<a id="step8">

# Step 8: Standoffs

Simple step. If you are using the full-sized acrylic guard, then each of the six screwholes will be set up like this:

![Step 8: Standoffs](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/8-0.png?raw=true "Step 8: Standoffs")

If you are using one of the partial guards, then you will take the female-female 8mm standoffs and use them instead of the male-female 8mm standoffs at the bottom and top right if you are using the half top guard. With the full top guard, you will use all three top ones with the male-female ones.

![Step 8: Standoffs](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/8-1.png?raw=true "Step 8: Standoffs")


<a id="step9">

# Step 9: Bottom and Feet

Put the bottom on and then the four rubber feet. The screws pass through the switch plate like shown in these pictures.

![Step 9: Bottom and Feet](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/9-0.png?raw=true "Step 9: Bottom and Feet")


<a id="step9">

# Step 10: Acrylic Guard

Install the acrylic guard of your choice now. If it has blue film on it (it probably does by default) then peel it off like this:

![Step 10: Acrylic Guard](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/10-0.png?raw=true "Step 10: Acrylic Guard")

Guard on!

![Step 10: Acrylic Guard](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/10-1.png?raw=true "Step 10: Acrylic Guard")


<a id="step10">

# Step 11: Keycaps and Submit For Inspection

All done! Put the keycaps on then have your cat check it over for approval. Enjoy!

![Step 11: Keycaps and Submit For Inspection](https://github.com/MechWild/build_guides/blob/main/keyboards/bbpad/pictures/steps/finished.png?raw=true "Step 11: Keycaps and Submit For Inspection")