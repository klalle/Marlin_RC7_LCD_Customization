# Marlin_RC7_LCD_Customization for MPCNC-router
This is a customization of the LCD-menu that's in the project "RC7_MPCNC_LCD_9916" from:

http://www.vicious1.com/marlin-firmware/ 

the code is downloaded from: "Use this one for now- Marlin RC7 MPCNC w/LCD" which directs to: 
http://www.vicious1.com/wp-content/uploads/2015/12/RC7_MPCNC_LCD_9916.zip

I was going crazy when trying to access the menu objects I needed through the LCD, so I came up with a couple of improvements that customized the menu for me. 
This is what I tried to accomplish:
• Get rid of all junk I don’t use (I’m only using the machine as a CNC-router)
• Reorder the menu to put the mostly used commands on top
• Access the z-probe offset from the LCD-menu
  o The height of the piece of metal I let the tool go down against to probe for z (connected to GND and z-min)
• Make a temporary Z-offset-menu item
 o Useful if e.g. an engraving ends up too shallow – just make a temporary z-offset of -0.5 mm and run the same file again (it doesn’t lose x and y)
  o So that you don’t have to alter the z-probe offset
• “Go to home” command in menu
• Set current position to home (without offset) menu item
• Make the 2nd option on a submenu pre-selected
  o If I e.g. enter the submenu “Move Axis” from the “Prep-menu”– most likely my next action won’t be to go back to the prep-menu, but to press the first real option (2nd option) 