---
geometry: margin=1in
fontsize: 10pt
---
### Loading Firmware ###

Your board will come with the appropriate firmware loaded. To load new firmware you use the STM Flash Loader in the distribution package.

The following sequence of screen shots is self explanatory.

There are two ways to proceed:

* If you are updating firmware use the GCS and the "BOOTLOAD" button to place the Arm processor into bootload mode. Don't power cycle the Arm board. This is far more convenient than the second option especially if the board is buried inside a FW aircraft.
* Put a link on the **Boot0** pins and power up the board. This places the Arm processor in bootloader mode when powered up.

Set the baud rate to 115K and the COM port as necessary.

![STM1](graphics/STM1.JPG)

![STM2](graphics/STM2.JPG)

Select the STM32F4-1024K.

![STM3](graphics/STM3.JPG)

Select the hex file you wish to load. Set the radio button to "necessary pages".

![STM4](graphics/STM4.JPG)

![STM5](graphics/STM5.JPG)

Wait until the verify is complete. Remove power and then remove the Boot0 link. Verify that the new firmware responds using UAVXGS.










