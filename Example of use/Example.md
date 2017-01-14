# Wooden Remote control

This is a toy I made for my 10months old sun Emil: 
![alt text](https://github.com/klalle/Marlin_RC7_LCD_Customization/blob/master/Example%20of%20use/2017-01-13%2010.15.46.jpg "Remote")
![alt text](https://github.com/klalle/Marlin_RC7_LCD_Customization/blob/master/Example%20of%20use/2017-01-11%2023.24.06.jpg "Remote")

###This is how I used the menu:
1. Define the Z-probe bottom thikness:
  1. Z homing offset = 1.24 mm
  2. Store to EEPROM Saves the Z homing offset to eeprom so that it never have to be entered again!
2. Find X0, Y0, Z0
  1. Manually set machine where you want X0,Y0 (with “move axis” or by hand)
  2. “Probe for Z0″/”Zero All” (with my Z probes clipped to the bit and the probe bottom piece underneath!)
3. Facing: In F360 I had defined the Origin (x0y0z0) to the model top, and told the facing bit to face off to Z0. Since the surface of my stock piece was a bit uneven, there were parts that was lower than Z0 => need to use my Z0 offset!
  1. “Temp Z offset” = -0.5 mm (note that the Z value on Status screen now changed from e.g. 5mm to 5.5mm => Z0 is now 5.5 mm down!
  2. Run the Facing -gcode and if needed, decrease the offset even more and run again till smooth surface!
Bit: 6mm 4 flutes
Speed: 10 mm/s
4. Contour: I used the same bit again (need to get a longer 1/8 bit… for this) so no need for Z-probing this time.
  1. Just run the next gcode (no need to go to x0y0z0 first, just hit run!)
Speed: 10 mm/s.
Max ramp stepdown: 1.5 mm
5. Adaptive clearing: this time I had to change bit so my Z will be off! Before I changed bit, I made sure that the stepper motors were active – to not accidently fuck up my coordinates!
  1. I hadn’t altered the post processor yet, so my stepper where disabled =>
“Move axis”/”X”/”1mm”/+1mm and same for Y to trigger the motors!
  2. Moved Z to height where I could change the bit (manually or in menu) and changed the bit
c. “Probe for Z0″/”Zero only Z” – To probe for the new Z0. Be very careful not to Zero All!!!! This time the probing will find the actual Z0, and does not need any temporary offset (even though it’s not cleared in the menu in current version, but that doesn’t affect anything, take a look at status screen and see that it says Z5 after probing and not Z(5-temp offset)!)
d. Run the code!
Done in 2 passes (1.5 mm at a time)
3 mm bit (~1/8″).
Speed: 7.5 mm/s.
4. Engraving: with 45 degree 1/8″ engraving bit – used the same method when changing tool as last time!
Speed: 10 mm/s
I will flip the piece and repeat step 2 (facing) till my remote is free from the stock (except for the tabs to hold it there)