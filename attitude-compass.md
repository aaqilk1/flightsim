# Attitude/Compass Gauge

This page is to document the reverse engineering for the attitude/compass gauge. Altogether, this unit has 3 servos, the attitude pitch 
servo and potentiometer, attitude roll servo and potentiometer, and a single servo motor and pot for the magnetic compass and heading
indicator. 

Image 1 <front of gauge display>
Image 2 <rear of image display>
Image 3 <detail of miniature airplane> 


The first job was setting up a system so I could monitor figure out the calibration readout for the roll axis. After getting the appropriate
pot values for a series of pitch angles, I then got ChatGPT to come up with some Processing code that would let me control a little attitude 
display on the computer with arrow keys and have that reflected in the motor-driven gauge. 

The second job was getting the miniature aircraft of the attitude display properly displayed. The actual piece from the ATC-710 moved up and 
down on a rail attached to the metal panel, so there was nothing to hold it in place when the gauge was removed from the entire unit as the 
attachment hole was slighly bigger than the pin on the arm that would drivr it. 

My solution to this was to scan the miniature aircraft (just a flat piece of metal) and then create a mockup in Fusion360 that could be 3D printed. 
After confirming size and fitment, I printed it and used a small lighter to heat up the pin enough that it could be pushed into the PLA and sit snug.
The plastic miniature aircraft now sits perfectly on the pitch arm, allowing for debugging and reverse engineering. 
