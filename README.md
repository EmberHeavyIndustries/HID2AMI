# HID2AMI 
**If you like this project and want to contribute to its further development, please consider donate 1$ or 1EU (or more, if you wish; paypal friends & family, please)**. Donors will be added to the "firmware beta release" channel, and will receive all intermediate beta releases of firmware updates, between major "official" releases. Donors will also be allowed to request new features and improvements (subjet to author's discretion)


[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/EmberHeavyIndustries)


[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

**HID2AMI** is an **HID mouse to quadrature waveform converter** and **HID Gamepad adapter** for the Amiga (and AtariST also..) series of boards; it allows ANY modern HID mouse (not limited to PS/2-USB) and almost ANY (*) modern digital/analog Gamepad to be connected and enjoyed with our Amiga computers.

(*) At the moment it has been tested with most Logitech Wingman, Thrustmaster series Gamepads and PS3/PC Gamepad clones. Xbox Gamepad support have to be considered in future releases (Xbox pads does not strictly comply to HID protocol). Working for any and every existing Gamepad cannot be guaranteed, but if you find a Pad which does not work with HID2AMI, you are encouraged to contact the author and supply him its "HID Report Descriptor" to be investigated.



![Image of HID2AMI-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.v1.0.0-1-300.jpg) ![Image of HID2AMI-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.v1.0.0-2-300.jpg)

## **HOW DOES IT WORK** (in brief):

HID2AMI recognizes and manages any HID device connected to its USB interface; if the device is recognized as an HID mouse, then HID2AMI starts understanding live movements and button pressings of the peripheral, then converting both of them into proper quadrature waveforms (and Amiga mouse button pressings) which can be properly understood by the Amiga itself, as if a quadrature "Amiga" mouse was connected.

If the device is recognized as an HID gamepad, then HID2AMI maps pad's controls on the Amiga Joystick port/interface.
Gamepad's buttons are mapped evenly on Amiga button1/button2 inputs.

There is no need to manually configure the emulation mode: device recognition and operation mode switching are automatically performed by HID2AMI itself.


 ## **HW AND SCHEMATICS**
  
|   Flavour      | Current ver.  |                Features               |
| -------------- | ------------- | ------------------------------------- |
| HID2AMI LITE   |    v1.0.0     |   direct output to Amiga port lines   |
| HID2AMI DeLuxe |    v1.0.0     |   output lines driven by mosfet       |
  
 
  *(Two version of HID2AMI exist: Lite version (yellow) and DeLuxe version (blue). They are different in the way outputs to Amiga ports are buffered (DeLuxe version outputs go through mosfet buffers, for maximum compatibility with "weak" amigas).*


## **FIRMWARE**
  
|      Baseline        | Current ver.  |                Features              |
| -------------------- | ------------- | -------------------------------------|
| HID2AMI BOOTLOADER   |    v1.2.0     |   Enables DFU upgrade of APP         |
| HID2AMI APP          |    v1.5.2     |   see notes below                    |
  


Features of fw v1.5.2: 
- Unified firmware, self configuring according to board variant (Lite or DeLuxe);
- Automatic recognition of any HID mouse;
- Automatic recognition of any (!) HID joystick/gamepad;
- Full support for both USB 1.1 and USB 2.0 periperhals;
- Support for both digital (hatswitch) and analog x-y gamepad axis;
- Automatic emulation mode switch upon peripheral connection (no need of any manual settings);
- Self discover and mapping of pad buttons (limited to first 6);
- Easy firmware upgrade through (windows) PC USB interface;


## **DEVELOPMENT**

HID2AMI hardware and firmware were designed, developed and maintained by **Sampedenawa** on behalf of **EmberHeavyIndustries** (an evil worldwide company, whose mission is to rule the world by the mean of reviving Amiga computers), following a discussion born on Italian www.amigapage.it Amiga forum.


## **ASSEMBLY**

 ## **WARNING !!**
 
 **NEVER, NEVER, NEVER connect "both sides" of HID2AMI to a power source at the same time !**
 **This means: do not connect HID2AMI to a PC through the USB port while it is plugged into your Amiga joy or mouse port !**
 **If you want to upgrade your HID2AMI with bootloader or DFU mode, beware to disconnect it from your Amiga first !**
 


#### Starting from scratch
 - Get latest gerber files available and build the pcb with a service of your choice
 - Get the BOM and buy all needed components
 - Assemble your board (moderate soldering skills needed)
 - Put the board in DFU mode and upload bootloader (USB A-A cable, DFU drivers and a Windows PC needed)
 - Put the board in HID2AMI-DFU mode, get your personal board-license-unique-code
 - Get the HID2AMI APP from the author, by sending him a request together with your board-license-unique-code
 - Put the board in HID2AMI-DFU mode and upload the APP
 - Put the board in RUN mode
 - Plug in and enjoy !
 
#### DIY KIT
 - Assemble your board (moderate soldering skills needed)
 - Put the board in DFU mode and upload bootloader (USB A-A cable, DFU drivers and a Windows PC needed)
 - Put the board in HID2AMI-DFU mode, get your personal board-license-unique-code
 - Get the HID2AMI APP from the author, by sending him a request together with your board-license-unique-code
 - Put the board in HID2AMI-DFU mode and upload the APP
 - Put the board in RUN mode
 - Plug in and enjoy !
  
#### PREASSEMBLED BOARD
 - Just plug in and enjoy !

### ASSEMBLING REFERENCE DOCS

At first, look at a fully assembled board (please note some vacancies: not all pads shall be populated)

[Reference Board: TOP](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/20190105_151759_full.jpg "Reference Board: TOP")

[Reference Board: BOTTOM](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/20190105_151811_full.jpg "Reference Board: BOTTOM")

*tbd: detailed assembling and flashing instructions will be linked here*

## **LICENSE TERMS**
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

### **Schematics and pcb gerbers**
of HID2AMI are open source, released under the Creative Commons CC BY-NC license.
This means that you are free to:

|                      |                                                                        |
| -------------------- | ---------------------------------------------------------------------- |
|      SHARE           |      copy and redistribute the material in any medium or format        |
|      ADAPT           |      remix, transform, and build upon the material                     |

      
Under the following terms:

|                       |                                                                        |
| --------------------- | ---------------------------------------------------------------------- |
|     Attribution       | You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use. |
|      NonCommercial    | You may not use the material for commercial purposes.                  |
|      ShareAlike       | If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.          |
| No additional restrict| You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.  |


### **HID2AMI BOOTLOADER** 
is free to download, copy and redistribuite.

### **HID2AMI APP** 
is distribuited by request from the author; each instance is strictly tied 1:1 to a particular HID2AMI board. You are not allowed to copy and distribuite HID2AMI APP in any medium or format. 



## **Warranty Disclaimer and Limitation of Liability**

HID2AMI is an hobbyist project without any commercial intention; you understand that we cannot and do not guarantee or warrant neither the HID2AMI hardware (including but not limited to: schematics, gerbers, pcb, components, assembling, etc.) nor the HID2AMI software (bootloader, app, etc) from defects, breakage or loss of functionality. You are using HID2AMI under your exclusive risk and responsibility; please understand and AGREE that **WE WILL NOT BE LIABLE FOR ANY LOSS OR DAMAGE CAUSED BY EITHER ANY USE OR ANY MISUSE OF HID2AMI**

BY MAKING USE OF HID2AMI, YOU EXPRESSLY AGREE THAT YOUR WILL ACCEPT IT ON "AS IS" BASIS WITHOUT ANY WARRANTIES OF ANY KIND, EITHER EXPRESS OR IMPLIED. YOU ALSO EXPRESSELY AGREE THAT YOUR USE OF HID2AMI HARDWARE AND ITS SOFTWARE COMPONENTS IS AT YOUR OWN RISK. NEITHER THE AUTHOR (Sampedenawa) NOR ANY PERSON ASSOCIATED WITH THE AUTHOR MAKES ANY WARRANTY OR REPRESENTATION WITH RESPECT TO THE COMPLETENESS, SECURITY, RELIABILITY, QUALITY, ACCURACY OR AVAILABILITY OF THE HID2AMI HARDWARE/SOFTWARE.

IF YOU DO NOT UNDERSTAND AND EXPRESSLY AGREE WHAT STATED ABOVE, YOU ARE NOT ENTITLED BY THE AUTHOR TO USE HID2AMI FOR ANY PURPOSE.
