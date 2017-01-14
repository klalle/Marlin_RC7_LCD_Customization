#Here's how you do it:

1. Download Marlin version [RC7_MPCNC_LCD_9916.zip](http://www.vicious1.com/wp-content/uploads/2015/12/RC7_MPCNC_LCD_9916.zip) from Vicious.

2. Download latest version of [U8glib x.xx (Arduino Environment)](https://code.google.com/archive/p/u8glib/downloads)
  * Add to your Arduino library

3. Unzip the "RC7_MPCNC_LCD_9916.zip"

4. Downoad the modified files from the "Marlin"-directory and replace the originial files in the RC7_MPCNC_LCD_9916 with them.

5. Compile and upload the Marlin firmware in the Arduino IDE to your Arduino/Ramps-board!

###And you're done!


If you want, you can always change back to the original version by uploading that one, or customize it yourselves to suit your needs...

All changes I've made are marked with //Kalle - open it up in Notepad++ and do a search!

All menu-changes are done in "Marlin/ultralcd.cpp"

The only change I've made in Marlin/Configuratio_adv.h is to set SD_FINISHED_STEPPERRELEASE to false to keep the steppers active after file is finnished.

The Post processor is modified to not reset home (X0,Y0,Z0) at start of file, and to not insert M84 (Disable steppers) at the end of file.