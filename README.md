# HID2AMI 
**If you like this project and want to contribute to its further development, please consider donate 1$ or 1EU (or more, if you wish; paypal friends & family, please).** 

Donors will be added to the "firmware beta release" channel, and will receive all intermediate beta releases of firmware updates, between major "official" releases. Donors will also be allowed to request new features and improvements (subjet to author's discretion).

| [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/EmberHeavyIndustries)||[![Email, Contacts & Requests](https://github.com/EmberHeavyIndustries/Depot/blob/master/Pics/EmailSticker.jpg?raw=true)](mailto:EmberHEavyIndustries@gmail.com)|
| ------------------------------ | ---------------------------------------------- | --------------------------- |


[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)


**HID2AMI** is an **HID mouse to quadrature waveform converter** and **HID Gamepad adapter** for the Amiga (and AtariST also..) series of boards; it allows ANY modern HID mouse (not limited to PS/2-USB) and almost ANY (*) modern digital/analog Gamepad to be connected and enjoyed with our Amiga computers.

(*) At the moment it has been tested with most Logitech Wingman, Thrustmaster series Gamepads and PS3/PC Gamepad clones. Xbox Gamepad support have to be considered in future releases (Xbox pads does not strictly comply to HID protocol). Working for each and every existing Gamepad cannot be guaranteed, but if you find a Pad which does not work with HID2AMI, you are encouraged to contact the author and supply him its "HID Report Descriptor" to be investigated.



![Image of HID2AMI-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.v1.0.0-1-300.jpg) ![Image of HID2AMI-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.v1.0.0-2-300.jpg)

## **HOW DOES IT WORK** (in brief):

HID2AMI recognizes and manages any HID device connected to its USB interface; if the device is recognized as an HID mouse, then HID2AMI starts capturing live movements and button pressings of the peripheral, then converting both of them into proper quadrature waveforms (and Amiga mouse button pressings) which can be properly understood by the Amiga itself, as if a real quadrature "Amiga" mouse was connected.

If the device is recognized as an HID gamepad, then HID2AMI maps pad's controls on the Amiga Joystick port/interface.
Gamepad's buttons are mapped evenly on Amiga button1/button2 inputs.

There is no need to manually configure the emulation mode: device recognition and operation mode switching are automatically performed by HID2AMI itself.


 ## **HW AND SCHEMATICS**
  
|   Flavour      | Current ver.  |                Features               |
| -------------- | ------------- | ------------------------------------- |
| HID2AMI LITE   |    v1.0.0     |   direct output to Amiga port lines   |
| HID2AMI DeLuxe |    v1.0.0     |   output lines driven by mosfet       |
  
 
  *Two version of HID2AMI exist: Lite version (yellow) and DeLuxe version (blue). They are different in the way outputs to Amiga ports are buffered (DeLuxe version outputs go through mosfet buffers, for maximum compatibility with "weak" amigas).*


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

(!) HID2AMI has been tested against a number of HID compliant Gamepads; the following compatibility list keeps track of tested peripherals. If you tested your mice/Gamepads and want to contribute to the list, simply send an email to the author with your compatibility results. Thanks !

|      Device      |                Model               | HID2AMI fw version | Working |                Notes                 |     |
| ---------------- | ---------------------------------  |----------- | ------- | -------------------------------------| --- |
| Mice             | Any HID Compliant Mouse            |  v1.0.0    |  YES    | Any HID mouse                        |![MOU](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HID.HP.Mouse_200.jpg)|
| Gamepad          | Logitech Wingman Rumblepad         |  v1.3.0    |  YES    | Both digital and analog mode         |![WRP](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Wingman.Rumblepad_200.jpg)|
| Gamepad          | PS3/PC Clones                      |  v1.5.2    |  YES    | Both digital and analog mode         |![PS3CLONE](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.PS3.Clone_200.jpg)|
| Gamepad          | Thrustmaster Firestorm Digital     |  v1.3.0    |  YES    | Pad is digital only                  |![THFS](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Thrustmaster.Firestorm_200.jpg)|
| Gamepad          | Thrustmaster Wireless dual trigger |  v1.3.0    |  YES    | Both digital and analog mode         |![THWD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Thrustmaster.Wireless_200.jpg)|
| Gamepad          | XBOX 360 Clone                     |  v-.-.-    | NOT YET | Not HID protocol compliant           |     |


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
 - Put the board in DFU mode and upload bootloader (USB A-A cable, DFU drivers and a Windows PC needed) *(a)*
 - Put the board in HID2AMI-DFU mode, get your personal board-license-unique-code
 - Get the HID2AMI APP from the author, by sending him a request together with your board-license-unique-code
 - Put the board in HID2AMI-DFU mode and upload the APP *(b)*
 - Put the board in RUN mode
 - Plug in and enjoy !
 
#### DIY KIT
 - Assemble your board (moderate soldering skills needed)
 - Put the board in DFU mode and upload bootloader (USB A-A cable, DFU drivers and a Windows PC needed) *(a)*
 - Put the board in HID2AMI-DFU mode, get your personal board-license-unique-code
 - Get the HID2AMI APP from the author, by sending him a request together with your board-license-unique-code
 - Put the board in HID2AMI-DFU mode and upload the APP *(a)*
 - Put the board in RUN mode
 - Plug in and enjoy !
  
  *(a) The bootloader need to be flashed only once in each HID2AMI's board lifetime*
  
  *(b) The HID2AMI APP can be flashed at any new firmware release*
  
#### PREASSEMBLED BOARD
 - Just plug in and enjoy !

### ASSEMBLING REFERENCE DOCS

At first, look at a fully assembled board (please note some vacancies: not all pads shall be populated)

[Reference Board: TOP](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/20190105_151759_full.jpg "Reference Board: TOP")

[Reference Board: BOTTOM](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/20190105_151811_full.jpg "Reference Board: BOTTOM")

#### **SCHEMATICS**

[HID2AMI v1.0.0 SCHEMATICS SHEET](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.pdf)

#### **REFERENCE LAYOUTS**

[Reference Layout v1.0.0 Top](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.layout.top.pdf)

[Reference Layout v1.0.0 Bottom](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.layout.bottom.pdf)

#### **BILL OF MATERIALS**

|Part   |   Value  |     Device       |  Package   |   Note   | 
|-------|--------- |------------------|------------|----------|
|BOOT0  |   JP2E   |        JP1       |   JUMPER   |          |
|PA9BOOT|   JP2E   |        JP2       |   JUMPER   |          |
|       |          |                  |            |          |
|C1     | 100n     |   C-EUC0805      |  C0805     | Optional |
|C2     | 10u      |   C-EUC1206      |  C1206     | Optional |
|C3     | 100n     |   C-EUC0805      |  C0805     | Optional |
|C4     | 10u      |   C-EUC1206      |  C1206     | Optional |
|C5     | 100n     |   C-EUC0805      |  C0805     | MANDATORY|
|C6     | 100n     |   C-EUC0805      |  C0805     | MANDATORY|
|C7     | 22p      |   C-EUC0805      |  C0805     | MANDATORY|
|C8     | 22p      |   C-EUC0805      |  C0805     | MANDATORY|
|C9     | 10u      |   C-EUC1206      |  C1206     | Optional |
|C10    | 10u      |   C-EUC0805      |  C0805     | Optional |
|C11    | 100n     |   C-EUC0805      |  C0805     | MANDATORY|
|C12    | 100n     |   C-EUC0805      |  C0805     | MANDATORY|
|C13    | 100n     |   C-EUC0805      |  C0805     | Optional |
|C14    | 10u      |   C-EUC1206      |  C1206     | Optional |
|C15    | 100n     |   C-EUC0805      |  C0805     | Optional |
|C16    | 10u      |   C-EUC1206      |  C1206     | Optional |
|       |          |                  |            |          |
|IC1    |LM1117-3.3|   LM1117MPX-3.3  |  SOT223    | MANDATORY|
|       |          |                  |            |          |
|LED1   |          |   LEDSML0805     |  SML0805   | Optional |
|LED2   |          |   LEDSML0805     |  SML0805   | Optional |
|       |          |                  |            |          |
|Q1     | 8MHz     |   CRYSTALHC49S   |  HC49/S    | MANDATORY|
|       |          |                  |            |          |
|Q2     | BSS138   |   BSS138         |  SOT23     | MANDATORY|
|Q3     | BSS138   |   BSS138         |  SOT23     | MANDATORY|
|Q4     | BSS138   |   BSS138         |  SOT23     | MANDATORY|
|Q5     | BSS138   |   BSS138         |  SOT23     | MANDATORY|
|Q6     | BSS138   |   BSS138         |  SOT23     | MANDATORY|
|Q7     | BSS138   |   BSS138         |  SOT23     | MANDATORY|
|Q8     | BSS138   |   BSS138         |  SOT23     | MANDATORY|
|       |          |                  |            |          |
|R1     | 0k       |   SHORT          |  M805      | MANDATORY|
|R2     | 100k     |   R-EU_M0805     |  M805      | MANDATORY|
|R3     | 0k       |   SHORT          |  M805      | MANDATORY|
|R4     | 1k-10k   |   R-EU_M0805     |  M805      | Optional |
|R5     | 1k-10k   |   R-EU_M0805     |  M805      | Optional |
|R6-R12 | ---      |   --             |  --        | NA       |
|R13    | 100      |   R-EU_M0805     |  M805      | MANDATORY|
|R14    | 100      |   R-EU_M0805     |  M805      | MANDATORY|
|R15    | 100      |   R-EU_M0805     |  M805      | MANDATORY|
|R16    | 100      |   R-EU_M0805     |  M805      | MANDATORY|
|R17    | 100      |   R-EU_M0805     |  M805      | MANDATORY|
|R18    | 100      |   R-EU_M0805     |  M805      | MANDATORY|
|R19    | 100      |   R-EU_M0805     |  M805      | MANDATORY|
|R20    | 0k       |   SHORT          |  M805      | MANDATORY|
|       |          |                  |            |          |
|U1     | F105RBT6 |   STM32F105RBT6  |  TQFP64    | MANDATORY|
|       |          |                  |            |          |
|X1     |          |   USB-CONNECTOR  |            |          |
|X3     |          |   F09HP D-SUB9   |  F09HP     | MANDATORY|
|       |          |                  |            | MANDATORY|

### **GERBER FILES**

[HID2AMI v1.0.0 DELUXE GERBER FILES](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist_2019-01-19.zip)


### **FLASHING INSTRUCTIONS**

#### **PREREQUISITES**
In order to be able to flash both the bootloader and the HID2AMI app, you need:
- A MS-Windows PC
- An A-A USB cable (https://www.google.com/search?q=a-a+usb+cable)
- The free ST DFU Tools. Download the package from here (https://www.st.com/en/development-tools/stsw-stm32080.html)

#### **FLASHING THE BOOTLOADER**
- Install the ST DFU Tool package on your Windows machine. Make sure you have the ST DFU-USB driver installed (in case something went wrong, you can manually install them from the DFU Tool's directory)
- Put HID2AMI in DFU-BOOT mode, by selecting position 2-3 for both "BOOT0" and "PA9BOOT" jumpers
- MAKE SURE THAT HID2AMI IS NOT CONNECTED TO YOUR AMIGA MOUSE/JOY PORT
- Connect HID2AMI to any USB port of your PC, by mean of the A-A USB Cable
- After few seconds, HID2AMI should be recognized by Windows as "ST Device in DFU Mode"
- Launch "DfuSeDemo" App from ST Tools package. You should see a form like this one, showing your HID2AMI has booted in DFU mode and has been recognized properly  ![DFU-BOOT](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/50-01.Dfu.Boot.jpg)
- Select the HID2AMIBOOTLOADER.dfu file you previosly downloaded from [here] (https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Firmware/HID2AMIBOOTLOADER.dfu) by pressing "Choose" under "Upgrade or Verify Action". 
You should come to a condition like this  ![DFU-BOOT-INJECT](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/50-02.Dfu.Bootloader.inject.jpg)
- Press "Upgrade" button and waity the process to finish with success.






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
