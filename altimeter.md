# Altimeter
 
This file will go over all of the reverse engineering for the altimeter module found on the ATC-710. As with the other motor/servo-driven instruments, this one contains
a 12V DC motor/gearbox module and continously rotating 50k-ohm potentiometer. For the altimeter specifically, it seems that the needles are connected to a clock mechanism
which causes the "thousands" hand to move 1 number for every full revolution of the "hundreds" hand. Interestingly enough, it seems that the potentiometer is connected to 
the thousands hand so the readout *should* be consistent for altitudes from 0-10.000ft. There is also a momentary switch that can be heard clicking at 2 and 8 on the dial.

One issue that will probably present itself later is what the potentiometer will read as it gets close to the wrap point. This is probably why the momentary switch is part
of the mechanism. 

Here are some photos of the altimeter gauge removed from the main chassis. There is a barometer readout on the front that can be adjusted with the knob but it doesnt seem to
be connected to any of the potentiometers. I could potentially (hah!) connect a pot/hall effect sensor/rotary encoder to it later to compensate for barometric pressure and 
plug that information into the sim. 

<Image 1: front of altimeter dial> 

<Image 2: rear of altimeter dial>

To test the altimeter and figure out the potentiometer reading, I set it up to an arduino with a cheap L293D motor driver shield. 

<Image 3: test bed/setup>

