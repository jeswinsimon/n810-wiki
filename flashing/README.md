# Flashing Nokia N810

The [last time I messed up](http://talk.maemo.org/showthread.php?p=1490074) I used the Nokia Internet Tablet Software Update Wizard, an official tool from Nokia, for reflashing the device. It is [no longer available](http://europe.nokia.com/A4305010), Thank you Microsoft! 

There is no longer any option to flash the device in Mac OS, **770Flasher** is built for **PowerPC** and **Flasher-3.5** does not work with newer versions of Mac OS. So I borrowed a Windows 7 machine to try my luck with **Flasher-3.5** on Windows again.

### Required files:

- Flasher-3.5.exe
- RX-44_DIABLO_5.2008.43-7_PR_COMBINED_MR0_ARM.bin - Maemo 4.1 firmware for N810.
- libusb-win32-bin-1.2.6.0.zip

### The process:

1. Install Flasher-3.5 for Windows.
2. Navigate to the installation folder of Flasher and open a command window.
3. Fully charge your Nokia N810 and shut it down.
4. Connect the USB cable to the device and Computer.
5. Power up the device while holding down the Swap key(The button with two overlapping rectangles right below the camera).

   *The Screen will turn on with a NOKIA logo and a USB icon on the top right corner. The device is now in Flashing Mode.*

6. Execute `flasher-3.5.exe -F RX-44_DIABLO_5.2008.43-7_PR_COMBINED_MR0_ARM.bin -f -R`

   *The last time the Flasher was stuck on searching for device and could not identify the connected device. The following needs to be done if this happens*

7. Extract **libusb-win32-bin-1.2.6.0.zip** and run **inf-wizard.exe** located within the *bin* folder.
8. Click *next* and then select *Nokia N810 (Update Mode)* from the list shown. 
9. Click *next* for the next two windows. 
10. Save the *.inf* file.
11. Click *Install Now*.
12. You will be shown a warning message. Click *Install this driver software anyway*.
13. You will be shown an *Installation successful.* message. Rerun flasher now. 
   
*In my case I had Fasher running while I did steps 7-12. Flasher identified the device while the driver installation was running and proceeded with Flashing.*

### Source links:
[http://wiki.maemo.org/Updating_the_firmware](http://wiki.maemo.org/Updating_the_firmware#All_Systems)
[http://talk.maemo.org/showpost.php?p=849980&postcount=20](http://talk.maemo.org/showpost.php?p=849980&postcount=20)