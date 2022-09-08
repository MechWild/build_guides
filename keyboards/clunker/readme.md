# Clunker Build Guide
40% + half numrow + knob + solenoid

Chaos is fun and clunky.

![Finished Build](https://github.com/MechWild/build_guides/blob/main/keyboards/clunker/pictures/steps/step14-0.png?raw=true "Finished Build")

# Table of Contents
- [Disclaimer](#user-content-disclaimer)
- [Required Tools and Components](#required)
- [Recommended Tools](#recommended)
- [Kit Contents](#contents)
- [Step 0: Test and Flash Your Pro Micro](#step0)
- [Step 1: Resistor](#step1)
- [Step 2: Transistor](#step2)
- [Step 3: Pro Micro PINS (and only the pins)](#step3)
- [Step 4: Reset Button](#step4)
- [Step 5: Flyback Diode](#step5)
- [Step 6: Solenoid](#step6)
- [Step 7: Diodes](#step7)
- [Step 8: Encoder](#step8)
- [Step 9: Stabilizers](#step9)
- [Step 10: That one switch that is in the way](#step10)
- [Step 11: Pro Micro](#step11)
- [Step 12: The rest of the switches](#step12)
- [Step 13: Standoffs, Acrylic, Feet](#step13)
- [Step 14: Keycaps](#step14)



<a id="disclaimer">
 
# Disclaimer

The solenoid used on this board is VERY power hungry. The flyback diode and transistor are specifically to keep it from damaging your computer's USB port, BUT it might pull too much power for some USB ports. If it seems to disconnect when it is being used, try a different port and different USB cable first.

If you continue to have issues, please stop on by our Discord server and ask for help.

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

![PCB](pictures/parts/pcb.png?raw=true "PCB")

- Bottom

![Bottom](pictures/parts/bottom.png?raw=true "Bottom")

- Plate

![Plate](pictures/parts/plate.png?raw=true "Plate")


### Components

- Pro Micro

![Pro Micro](pictures/parts/promicros.png?raw=true "Pro Micro")

- Diodes (60)

![Diodes (60)](pictures/parts/diodes.png?raw=true "Diodes (60)")

- 1.5KOhm Resistor

![1.5KOhm Resistor](pictures/parts/resistor.png?raw=true "1.5KOhm Resistor")

- TIP102 Transistor

![TIP102 Transistor](pictures/parts/tip102.png?raw=true "TIP102 Transistor")

- SR306 Flyback Diode

![SR306 Flyback Diode](pictures/parts/sr306.png?raw=true "SR306 Flyback Diode")

- Solenoid

![Solenoid](pictures/parts/solenoid.png?raw=true "Solenoid")

- Encoder

![Encoder](pictures/parts/encoder.png?raw=true "Encoder")

- Knob

![Knob](pictures/parts/knob.png?raw=true "Knob")

- Reset Button

![Reset Button](pictures/parts/button.png?raw=true "Reset Button")


### Assembly Hardware

- 6x M2 8mm+3mm male female standoffs

![M2 8mm+3mm](pictures/parts/standoff8mm_mf.png?raw=true "M2 8mm+3mm")

- 7x M2 8mm female female standoffs

![M2 8mm](pictures/parts/standoff8mm.png?raw=true "M2 8mm")

- 3x M2 15mm standoffs

![M2 15mm](pictures/parts/standoff15mm.png?raw=true "M2 15mm")

- 3x M2 12mm standoffs

![M2 12mm](pictures/parts/standoff12mm.png?raw=true "M2 12mm")

- 6x M2 8mm screws

![M2 8mm screws](pictures/parts/longscrew.png?raw=true "M2 8mm screws")

- 14x M2 4mm screws

![M2 4mm screws](pictures/parts/shortscrew.png?raw=true "M2 4mm screws")

- 4x Rubber bumpons (feet)

![Rubber bumpons](pictures/parts/bumpons.png?raw=true "Rubber bumpons")



<a id="step0">

# Step 0: Test and Flash Your Pro Micro

Firmware is on our firmware repo, available here:
[https://github.com/MechWild/mw_firmware/releases](https://github.com/MechWild/mw_firmware/releases)

This general guide will be moved to Github soon, but for now check out the guide here:
[https://mechwild.com/guides/general/flashing-a-pro-micro/](https://mechwild.com/guides/general/flashing-a-pro-micro/)


<a id="step1">

# Step 1: Resistor
![Step 1: Resistor](pictures/steps/step1-0.png?raw=true "Step 1: Resistor")

Yes. This first step is the easiest one. It doesn't matter which way this is facing.


<a id="step2">

# Step 2: Transistor
Bend the legs of the transistor to be about 90 degrees right around the part where the leg start to widen.

![Step 2: Transistor](pictures/steps/step2-0.png?raw=true "Step 2: Transistor")

Put it in the board and solder it in place (make sure to clip the excess legs with your flush cutters)

![Step 2: Transistor](pictures/steps/step2-1.png?raw=true "Step 2: Transistor")


<a id="step3">

# Step 3: Pro Micro PINS (and only the pins)

## This is VERY important! 

ONLY SOLDER THE PINS INTO PLACE. DO NOT SOLDER THE PRO MICRO ON AS WELL YET. WE WILL BE DOING THAT LATER.

![Step 3: Pro Micro PINS (and only the pins)](pictures/steps/step3-0.png?raw=true "Step 3: Pro Micro PINS (and only the pins)")

![Step 3: Pro Micro PINS (and only the pins)](pictures/steps/step3-1.png?raw=true "Step 3: Pro Micro PINS (and only the pins)")

![Step 3: Pro Micro PINS (and only the pins)](pictures/steps/step3-2.png?raw=true "Step 3: Pro Micro PINS (and only the pins)")


<a id="step4">

# Step 4: Reset Button
![Step 4: Reset Button](pictures/steps/step4-0.png?raw=true "Step 4: Reset Button")

Ok. I might have lied on step 1. This might be the easiest step.


<a id="step5">

# Step 5: Flyback Diode

Bend the legs as close to the body of the diode as you can at around 90 degrees.

![Step 5: Flyback Diode](pictures/steps/step5-0.png?raw=true "Step 5: Flyback Diode")

The direction DOES matter for this one! The thick bar on the diode needs to match up with the line on the PCB!

![Step 5: Flyback Diode](pictures/steps/step5-1.png?raw=true "Step 5: Flyback Diode")


<a id="step6">

# Step 6: Solenoid

Well, here we go. The most complicated step. Read through this entire step before cutting anything!

First, we will be cutting the end of the wires off the solenoid so that we still have 1 to 2 inches (3mm to 5mm) of slack. 

I then like to tie the wires into a loose knot so that it doesn't seem as long when put on the board.

![Step 6: Solenoid](pictures/steps/step6-0.png?raw=true "Step 6: Solenoid")

Then you will need to strip the very ends of the wires about 1/4" (5mm) or so and tin the tips. 

Tinning the tips of the wire is where you apply some solder to the exposed wire ends so that they are 

basically one solid piece instead of a bundle of wires that spreads apart. 

This will make it easier to solder to the PCB.

![Step 6: Solenoid](pictures/steps/step6-1.png?raw=true "Step 6: Solenoid")

Next we are going to put the wires through the holes from the top of the PCB, and solder the tinned ends from the bottom. 

It does not matter which wire goes in which hole here.

![Step 6: Solenoid](pictures/steps/step6-2.png?raw=true "Step 6: Solenoid")

Now we will be securing the solenoid to the PCB. The solenoid has two threaded holes on the bottom that should align with the two holes on the PCB to the right of where you soldered the wires. Use the SHORT screws (4mm) to secure the solenoid by passing screws through the PCB from the bottom into the solenoid on the top side of the PCB.

![Step 6: Solenoid](pictures/steps/step6-3.png?raw=true "Step 6: Solenoid")

The bottom of the PCB near Huynh/Silly name logo should look like this for those screws once they are both in correctly

![Step 6: Solenoid](pictures/steps/step6-4.png?raw=true "Step 6: Solenoid")

At this point, I like to loosen up the knot a little and get it positioned in a way that I like that looks good. Make sure that the knot does not hit the metal plunger that extends out the back of the solenoid or it might affect the way it sounds.

![Step 6: Solenoid](pictures/steps/step6-5.png?raw=true "Step 6: Solenoid")


<a id="step7">

# Step 7: Diodes

This step is also easy, but time consuming. The direction of each diode matters and the black line on the diode should match up with the black line on the silkscreen on the PCB.

![Step 7: Diodes](pictures/steps/step7-0.png?raw=true "Step 7: Diodes")

Do them all. This is how it should look. Note that the Pro Micro is STILL not on the board, on purpose.

![Step 7: Diodes](pictures/steps/step7-1.png?raw=true "Step 7: Diodes")


<a id="step8">

# Step 8: Encoder

If you are using an encoder, put it on now. If you are using a switch here instead, it can wait until step 12.

![Step 8: Encoder](pictures/steps/step8-0.png?raw=true "Step 8: Encoder")


<a id="step9">

# Step 9: Stabilizers

Put any stabilizers that you want to use for your chosen layout on the board now. 

If you are unsure about which holes go to which layouts, try doing a test fit before soldering anything into place. 

If you still can't figure it out, feel free to stop by our Discord server and ask for help.

![Step 9: Stabilizers](pictures/steps/step9-0.png?raw=true "Step 9: Stabilizer")


<a id="step10">

# Step 10: That one switch that is in the way

Ok, so here is the reason we didn't solder the Pro Micro on to the board yet. There is one switch that is over where the Pro Micro gets mounted. It CAN be soldered on after the Pro Micro is in place, but it is safer to do it beforehand. If you soldered your Pro Micro on already, you can still salvage it, so don't worry. Just be careful to not push your iron against the Pro Micro while you are soldering the switch.

First thing I would like to point out, in case you forgot, is that switches go THROUGH the switch plate. You could choose not to use a switch plate for this board, but let's assume you aren't choosing to not use it.

I like to put several switches on the board around the corners and edges of the board. I DO NOT solder them in to place yet, and they are just there to keep the plate steady while I solder on the switch labeled "IMPORTANT!" in the picture below.

![Step 10: That one switch that is in the way](pictures/steps/step10-0.png?raw=true "Step 10: That one switch that is in the way")

Here is shot of the bottom where this switch is soldered into place, between the Pro Micro pins.

![Step 10: That one switch that is in the way](pictures/steps/step10-1.png?raw=true "Step 10: That one switch that is in the way")


<a id="step11">

# Step 11: Pro Micro

THE DIRECTION OF THE PRO MICRO MATTERS HERE. The Pro Micro goes on the BOTTOM of the PCB, with the components facing TOWARDS the PCB (so upwards).

Now we can solder the Pro Micro into place and test it. After you have it soldered on, plug it in and see if it works by connecting the spots for the switches with tweezers, or any of your normal tests for boards. 

Bonus is that by testing it this way, you should be able to see if the solenoid works too.

![Step 11: Pro Micro](pictures/steps/step11-0.png?raw=true "Step 11: Pro Micro")


<a id="step12">

# Step 12: The rest of the switches

Once you know the Pro Micro and the rest of the components are working, you can move on to solder the rest of the switches into place. 

Please make sure to test before this step, because fixing things is WAY easier before it is fully assembled.

![Step 12: The rest of the switches](pictures/steps/step12-0.png?raw=true "Step 12: The rest of the switches")


<a id="step13">

# Step 13: Standoffs, Acrylic, Feet

Not every standoff you receive will be used. This is to allow for other acrylic guard options we might want to use in the future, so don't be alarmed if you have bonus parts.

For this step, you will first be using the 12mm standoffs, the 15mm standoffs, and the 8mm Male/Female standoffs (those are the ones that have basically a screw built in to them, refer to the parts at the beginning of the guide for pictures.)

As shown in this picture, you will be putting the screw part of the 8mm Male/Female standoff through the board from the bottom, and then attaching the 12mm and 15mm standoffs to it so that they fasten tightly to the PCB.

![Step 13: Standoffs, Acrylic, Feet](pictures/steps/step13-0.png?raw=true "Step 13: Standoffs, Acrylic, Feet")

As shown here, the taller acrylic piece is supported by the 15mm standoffs, and the shorter piece uses the 12mm standoffs. Use the long screws (8mm) to attach the acrylic to the top of the long standoffs.

![Step 13: Standoffs, Acrylic, Feet](pictures/steps/step13-1.png?raw=true "Step 13: Standoffs, Acrylic, Feet")

The other 3 standoffs we will be putting on the board go in the following positions. Circled are the pass through holes that you will be putting the screw through and then attaching the 8mm standoffs to the bottom here. Note that these are the regular standoffs that have threaded holes on both ends and not the Male/Female ones.

![Step 13: Standoffs, Acrylic, Feet](pictures/steps/step13-2.png?raw=true "Step 13: Standoffs, Acrylic, Feet")

Flip the board over, attach the bottom to all the standoffs in the positions marked here, and then throw your rubber bumpons on the corners to use as feet. 

If you bought the aluminum feet to get it an angle, use the two larger holes that haven't been used yet to attach those with their included mounting screw.

![Step 13: Standoffs, Acrylic, Feet](pictures/steps/step13-3.png?raw=true "Step 13: Standoffs, Acrylic, Feet")


<a id="step14">

# Step 14: Keycaps

Keycap it up and get clunkin'.

![Step 14: Keycaps](pictures/steps/step14-0.png?raw=true "Step 14: Keycaps")

