# Clunker Build Guide
40% + half numrow + knob + solenoid

Chaos is fun and clunky.

![Finished Build](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/steps/step14-0.png?raw=true "Finished Build")

# Table of Contents
- [Required Tools and Components](#user-content-required)
- [Recommended Tools](#user-content-recommended)
- [Kit Contents](#user-content-contents)
- [Step 0: Test and Flash Your Pro Micro](#user-content-step0)
- [Step 1: Resistor](#user-content-step1)
- [Step 2: Transistor](#user-content-step2)
- [Step 3: Pro Micro PINS (and only the pins)](#user-content-step3)
- [Step 4: Reset Button](#user-content-step4)
- [Step 5: Flyback Diode](#user-content-step5)
- [Step 6: Solenoid](#user-content-step6)
- [Step 7: Diodes](#user-content-step7)
- [Step 8: Encoder](#user-content-step8)
- [Step 9: Stabilizers](#user-content-step9)
- [Step 10: That one switch that is in the way](#user-content-step10)
- [Step 11: Pro Micro](#user-content-step11)
- [Step 12: The rest of the switches](#user-content-step12)
- [Step 13: Standoffs, Acrylic, Feet](#user-content-step13)
- [Step 14: Keycaps](#user-content-step14)



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

![PCB](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/pcb.png?raw=true "PCB")

- Bottom

![Bottom](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/bottom.png?raw=true "Bottom")

- Plates

![Plate](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/plate.png?raw=true "Plate")


### Components

- BlackPill

![BlackPill](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/promicros.png?raw=true "Pro Micro")

- Diodes (60)

![Diodes (60)](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/diodes.png?raw=true "Diodes (60)")

- 1.5KOhm Resistor

![1.5KOhm Resistor](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/resistor.png?raw=true "1.5KOhm Resistor")

- TIP102 Transistor

![TIP102 Transistor](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/tip102.png?raw=true "TIP102 Transistor")

- SR306 Flyback Diode

![SR306 Flyback Diode](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/sr306.png?raw=true "SR306 Flyback Diode")

- Solenoid

![Solenoid](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/solenoid.png?raw=true "Solenoid")

- Encoder

![Encoder](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/encoder.png?raw=true "Encoder")

- Knob

![Knob](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/knob.png?raw=true "Knob")

- Reset Button

![Reset Button](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/button.png?raw=true "Reset Button")


### Assembly Hardware

- 6x M2 8mm+3mm male female standoffs

![M2 8mm+3mm](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/standoff8mm_mf.png?raw=true "M2 8mm+3mm")

- 7x M2 8mm female female standoffs

![M2 8mm](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/standoff8mm.png?raw=true "M2 8mm")

- 3x M2 15mm standoffs

![M2 15mm](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/standoff15mm.png?raw=true "M2 15mm")

- 3x M2 12mm standoffs

![M2 12mm](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/standoff12mm.png?raw=true "M2 12mm")

- 6x M2 8mm screws

![M2 8mm screws](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/longscrew.png?raw=true "M2 8mm screws")

- 14x M2 4mm screws

![M2 4mm screws](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/shortscrew.png?raw=true "M2 4mm screws")

- 4x Rubber bumpons (feet)

![Rubber bumpons](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/parts/bumpons.png?raw=true "Rubber bumpons")



<a id="step0">

# Step 0: Test and Flash Your BlackPill

Firmware is on our firmware repo, available here:
[https://github.com/MechWild/mw_firmware/releases](https://github.com/MechWild/mw_firmware/releases)

All black pills that we sell are tested and preflashed with a modified version of either the BBS firmware or OBE firmware. This is just so that you can plug it in and test to make sure it is connected to your computer correctly and then flash it before building the rest of the board. By default, the blue light on the front of the black pill will be connected to the Num Lock status indicator for your computer. Plug in the black pill, and toggle Num Lock with another keyboard to see if the light responds accordingly. 

Next, we will try and put it into bootloader mode. To do this, hold the button labeled “Boot0” on the top of the Blackpill, and while you are still holding that button, tap and release the “NRST” button. Then after a second or two, release the “Boot0” button. If nothing happens in QMK toolbox or if it still is responding when you push the Num Lock, then you should try again, because it didn’t go into bootloader mode.

Now we will try and flash the Blackpill using QMK toolbox (or your tool of choice.) Grab the appropriate firmware from the link at the beginning of this step, download it, select it in QMK Toolbox, put the BlackPill in bootloader mode then click flash.

<a id="step1">

# Step 1: OLED Headers (AND ONLY HEADERS)

![Step 1: OLED Headers](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step1.png?raw=true "Step 1: OLED Headers ")

For the first step, you are going to solder the OLED headers to the top of the PCB (the top of the PCB does not have an outline around where the BlackPill sits.) We are doing this because it makes it easier to attach the OLED later on once the other parts are in place.


<a id="step2">

# Step 2: Diodes

An easy but time consuming step. The direction of each diode matters and the black line on the diode should match up with the black line (or white line on black PCBs) on the silkscreen on the PCB. Make sure each diode is on the bottom of the PCB.

![Step 2: Diodes](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step2.png?raw=true "Step 2: Diodes")

Solder them in place, flip it to the front of the board, and clip the excess legs with your flush cutters.

<a id="step3">

# Step 3: Buttons

Put the buttons in the place marked for them on the top of the PCB. Flip the board, and solder them into place. The legs of the buttons go out the left and right side, so make sure they are oriented to go in that way.

![Step 3: Buttons](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step3.png?raw=true "Step 3: Buttons")

<a id="step4">

# Step 4: LED Resistors

You will have 3 220 Ohm resistors in your kit. They are marked with RED-RED-BLACK-BLACK-BROWN as the band colors. The direction they face doesn't matter and they go in positions R1, R2, R3 on the bottom of the PCB.

![Step 4: LED Resistors](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step4.png?raw=true "Step 4: LED Resistors")

<a id="step5">

# Step 5: Status LEDs (READ ENTIRE STEP)

The LEDs that the resistors are for go on top of the PCB and NORMALLY would align the flat edge of the LED with the silkscreen, however, the footprint for the LEDs was flipped for the initial production run and the LEDs need to go backwards from how they normally should be. That means you will have the flat edge of the LED facing away from the flat edge on the silkscreen. The direction for this step matters very much.

![Step 5: Status LEDs](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step5.png?raw=true "Step 5: Status LEDs")

<a id="step6">

# Step 6: GPIO Expander Resistors

Basically the same deal as the LED resistors, but these are a different value (10KOhm) so are marked with BROWN-BLACK-BLACK-RED-BROWN colored bands. The direction of these doesn't matter. I like putting these on the top of the board but they could go on the bottom if you wanted. These should be placed in positions R4 and R5.

![Step 6: GPIO Expander Resistors](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step6.png?raw=true "Step 6: GPIO Expander Resistors")

<a id="step7">

# Step 7: GPIO Expander IC Socket

Simple step. Direction matters. There is a little notch on one of the short ends of the socket's edge. That should face upwards. The socket goes on the top of the PCB next to the resistors from the previous step. 

![Step 7: GPIO Expander IC Socket](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step7.png?raw=true "Step 7: GPIO Expander IC Socket")

<a id="step8">

# Step 8: BlackPill

Now we put the BlackPill on the board. It goes on the bottom of the PCB and has the components face outwards (down) so that you can still push the buttons on it after it is soldered in place. USB port goes upwards, so it can be accessed.

![Step 8: BlackPill](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step8.png?raw=true "Step 8: BlackPill")

<a id="step9">

# Step 9: OLED

Now we put the OLED on those pins we soldered in the first step. No matter which style of OLED you have (narrow or wide one)it will face upwards towards the top edge of the board from the pins.

![Step 9: OLED](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step9.png?raw=true "Step 9: OLED")

<a id="step10">

# Step 10: Prep the Nugget

The Nugget and touchpad mounting ring will come attached to each other with break away tabs. You will need to break away the excess parts of the mounting ring and clean it up a little so it looks good for you (and lets the touchpad fit in the middle.)

Check out the red circled bits below for what need to be cleaned up.

![Step 10: Prep the Nugget](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step10.png?raw=true "Step 10: Prep the Nugget")

<a id="step11">

# Step 11: Solder your switches (and encoders if you are using them)!

We do the switches now because the Nugget sits below one of the switches, so they need to be soldered on before we continue. This is also an easy time to do the encoders you are interested in using, but you will have an easier time if you solder the switches on before the encoders because of how tall the encoders are.

NOTE: IF YOU ARE USING THE HALF PLATES, THE SWITCHES WILL NEED TO BE INSERTED THROUGH THE PLATE BEFORE BEING SOLDERED.

I will not be soldering switches in this guide, but please make sure to do this in order.

Please make sure to test before this step, because fixing things is WAY easier before it is fully assembled.

<a id="step12">

# Step 12: Solder the Nugget

Nugget goes under one of the switches at the bottom of the board, on the bottom of the PCB. It needs to be aligned so the 1 and 7 pin labels on the Nugget match the 1 and 7 pin labels on the PCB silkscreen.
You will ONLY be soldering the two rows of 6 pins on the left and right sides and not the row of 4 or 5 that are on top or bottom of the Nugget. 

![Step 12: Solder the Nugget](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step12.png?raw=true "Step 12: Solder the Nugget")

<a id="step13">

# Step 13: Mounting the TouchPad

There are two positions for the touchpad to be mounted. I will be using the top position for this guide. The short 3mm standoffs will go on the top of the board with female side facing upwards, and will be secured in place by a 10mm standoff screwed on the the male portion on the bottom of the PCB. There are 4 3mm standoff spots for each position that form a square shape. 

![Step 13: Mounting the TouchPad](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step13-0.png?raw=true "Step 13: Mounting the TouchPad")

Then you should be able to place the acrylic on the standoffs like so:

![Step 13: Mounting the TouchPad](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step13-1.png?raw=true "Step 13: Mounting the TouchPad")

The touchpad itself fits snugly inside the white ring that was around the Nugget from step 10. There is a small tab inside the ring that goes in to a small slot in the lip of the touchpad. Align then as such and then place it on top of the acrylic mounting ring with the tab position on the left side as you look at it:

![Step 13: Mounting the TouchPad](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step13-2.png?raw=true "Step 13: Mounting the TouchPad")

Sandwich the mounting ring by placing the other acrylic ring on top of it and then screwing it into place with the 6mm screws.

![Step 13: Mounting the TouchPad](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step13-3.png?raw=true "Step 13: Mounting the TouchPad")

<a id="step14">

# Step 14: Ribbon Cable

Now we need to connect the Nugget to the touchpad. This is easier once it is all mounted, which is why we are tackling it now. The grey lip on the ribbon connector on the Nugget itself will flip up a little. Slide one end of the ribbon cable (silver contacts facing down) into the connector and make sure it is aligned as straight-on with the connector as you can. Seat it properly, then close the connector tab. Then you will bring the cable up to the hole in the PCB that allows access to the ribbon cable mount on the touchpad itself. The contacts on the ribbon cable here will face to the right. Get a good grip and insert it in the mount as straight on as you can. 

![Step 14: Ribbon Cable](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step14.png?raw=true "Step 14: Ribbon Cable")

# Step 15: GPIO Expander

The GPIO expander need to be inserted into the socket you soldered in step 7. The notch on the expander aligns with the notch on the top of the socket. The pins will be a little too wide for the socket, so you will need to bend them in slightly (do it gently.)

Make sure it is fully seated in the socket and that the pins arent bent up and that they are fully inserted in the socket. Should look like this from the top.

![Step 15: GPIO Expander](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step15.png?raw=true "Step 15: GPIO Expander")

# Step 16: Case Assembly Hardware

NEEDS TO BE TYPED UP BECAUSE I FORGOT PICS. PUT ON STANDOFFS AND FEET. THROW KEYCAPS ON AND PARTY.

![Step 16: Case Assembly Hardware](https://github.com/MechWild/build_guides/blob/main/keyboards/bb65/pictures/steps/step16.png?raw=true "Step 16: Case Assembly Hardware")

