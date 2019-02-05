![HID2AMI](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HID2-AMI-Logo-Web-Show.png)

**If you like this project and want to contribute to its further development, please consider donate some $ or € (paypal friends & family, please or DO NOT select "Buying something" from money transfer frontpage).** 

Donors will be added to the "firmware beta release" channel, and will receive all intermediate beta releases of firmware updates, between major "official" releases. Donors will also be allowed to request new features and improvements (subjet to author's discretion).

| [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/EmberHeavyIndustries)||[![Email, Contacts & Requests](https://github.com/EmberHeavyIndustries/Depot/blob/master/Pics/EmailSticker.jpg?raw=true)](mailto:EmberHEavyIndustries@gmail.com)|
| ------------------------------ | ---------------------------------------------- | --------------------------- |


[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)


**HID2AMI** is an **HID mouse to quadrature waveform converter** and **HID Gamepad adapter** for the Amiga (and AtariST also..) series of boards; it allows ANY modern HID mouse (not limited to PS/2-USB) and almost ANY (*) modern digital/analog Gamepad to be connected and enjoyed with our Amiga computers.

(*) At the moment it has been tested with most Logitech Wingman, Thrustmaster series Gamepads and PS3/PC Gamepad clones, Xbox Gamepad clones (Xbox pads does not strictly comply to HID protocol). Working for each and every existing Gamepad cannot be guaranteed, but if you find a Pad which does not work with HID2AMI, you are encouraged to contact the author and supply him its "HID Report Descriptor" to be investigated.



![Image of HID2AMI-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.v1.0.0-1-300.jpg) ![Image of HID2AMI-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.v1.0.0-2-300.jpg) ![Image of HID2AMI-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.Black.Top_300.jpg) ![Image of HID2AMI-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.Black.Bottom_300.jpg)


## **HOW DOES IT WORK** (in brief):

HID2AMI recognizes and manages any HID device connected to its USB interface; if the device is recognized as an HID mouse, then HID2AMI starts capturing live movements and button pressings of the peripheral, then converting both of them into proper quadrature waveforms (and Amiga mouse button pressings) which can be properly understood by the Amiga itself, as if a real quadrature "Amiga" mouse was connected.

If the device is recognized as an HID gamepad, then HID2AMI maps pad's controls on the Amiga Joystick port/interface.
Gamepad's buttons are mapped evenly on Amiga button1/button2/UP (useful for jump & racing games) inputs.

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
| HID2AMI BOOTLOADER   |    v1.3.0     |   Enables DFU upgrade of APP         |
| HID2AMI APP          |    v1.7.1     |   see notes below                    |
  

Features of fw v1.7.1:
- Added mapping of DWN/backward to Gamepad 4th button. Buttons are now evenly mapped according P1->P2->UP->DWN sequence;
- User can swap UP<->DWN button mapping by simultaneously pressing first 4 pad's buttons;

Features of fw v1.6.2:
- Added mapping of UP/Forward to Gamepad 3rd button;
- Optimized gamepad decoding core, even faster response;

Features of fw v1.6.0:
- Added support for XBOX 360 Gamepad clones;
- Added support for MS Intellimouse;

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
| Mice             | Any HID Compliant Mouse            |  v1.0.0    |  YES    | Any HID mouse                        |![MOU](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HID.HP.Mouse_200.jpg)
| Mouse            | Microsoft Intellimouse             |  v1.6.0    |  YES    | Not HID protocol compliant           |![MOU](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Intellimouse_200.jpg)|
| Gamepad          | Logitech Wingman Rumblepad         |  v1.3.0    |  YES    | Both digital and analog mode         |![WRP](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Wingman.Rumblepad_200.jpg)|
| Gamepad          | PS3/PC Clones                      |  v1.5.2    |  YES    | Both digital and analog mode         |![PS3CLONE](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.PS3.Clone_200.jpg)|
| Gamepad          | Thrustmaster Firestorm Digital     |  v1.3.0    |  YES    | Pad is digital only                  |![THFS](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Thrustmaster.Firestorm_200.jpg)|
| Gamepad          | Thrustmaster Wireless dual trigger |  v1.3.0    |  YES    | Both digital and analog mode         |![THWD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Thrustmaster.Wireless_200.jpg)|
| Gamepad          | XBOX 360 Clone                     |  v1.6.0    | YES     | Not HID protocol compliant           |![XBOX](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.XBOX.360_200.jpg) |

## **DEVELOPMENT**

HID2AMI hardware and firmware were designed, developed and maintained by **Sampedenawa** on behalf of **EmberHeavyIndustries** (an evil worldwide company, whose mission is to rule the world by the mean of reviving Amiga computers), following a discussion born on Italian www.amigapage.it Amiga forum.


## **ASSEMBLY**

 ## **WARNING !!  A COUPLE THINGS YOU MUST UNDERSTAND BEFORE GOING FURTHER**
 
 - **NEVER, NEVER, NEVER connect "both sides" of HID2AMI to a power source at the same time !**
 **This means: do not connect HID2AMI to a PC through the USB port while it is plugged into your Amiga's joy/mouse port !**
 **If you want to upgrade your HID2AMI with bootloader or DFU mode, beware to disconnect it from your Amiga first !**
 
 - **BE AWARE** that when you connect a peripheral to the Amiga's mouse/joy port, the power supply or that peripheral comes from/through that port itself. Amiga control peripheral ports were probably not designed with "mega-rumble-end-of-universe-nuclear-powered" gamepads in mind: while there is generally no risk in connecting "common" mainstream peripherals like the ones have been tested (see above), be aware that improperly connecting an "high" power-demanding device could lead to overheat or even damage the Amiga joy/mouse port. You are usign HID2AMI at your own risk: I will either not be liable nor responsible for any damage you could cause to your hardware for any use or misuse of HID2AMI together with your systems.  
 


#### Starting from scratch
 - Get latest gerber files available and build the pcb with a service of your choice
 - Get the BOM and buy all needed components
 - Assemble your board (moderate soldering skills needed)
 - Put the board in DFU mode and upload bootloader (USB A-A cable, DFU drivers and a Windows PC needed) *(a)*
 - Put the board in BOOTLOADER mode, get your personal board-license-unique-code
 - Get the HID2AMI APP from the author, by sending him a request together with your board-license-unique-code
 - Put the board in BOOTLOADER mode and upload the APP *(b)*
 - Put the board in APP mode
 - Plug in and enjoy !
 
#### DIY KIT
 - Assemble your board (moderate soldering skills needed)
 - Put the board in DFU mode and upload bootloader (USB A-A cable, DFU drivers and a Windows PC needed) *(a)*
 - Put the board in BOOTLOADER mode, get your personal board-license-unique-code
 - Get the HID2AMI APP from the author, by sending him a request together with your board-license-unique-code
 - Put the board in BOOTLOADER mode and upload the APP *(a)*
 - Put the board in APP mode
 - Plug in and enjoy !
  
  *(a) The bootloader need to be flashed only once in each HID2AMI's board lifetime*
  
  *(b) The HID2AMI APP can be flashed at any new firmware release*
  
#### PREASSEMBLED BOARD
 - Just plug in and enjoy !

### ASSEMBLING REFERENCE DOCS

At first, look at a fully assembled board (please note some vacancies: not all pads shall be populated)

[Reference Board: TOP](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.Black.Top.jpg "Reference Board: TOP")

[Reference Board: BOTTOM](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.Black.Bottom.jpg "Reference Board: BOTTOM")

#### **SCHEMATICS**

[HID2AMI v1.0.0 SCHEMATICS SHEET](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.schermatics.pdf)

#### **REFERENCE LAYOUTS**

[Reference Layout v1.0.0 Top](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.layout.top.pdf)

[Reference Layout v1.0.0 Bottom](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.layout.bottom.pdf)

#### **BILL OF MATERIALS**

Components noted as "Optional" fulfil the general purpose STM32F1x reference design; generally speaking they can be safely omitted from the assembly of HID2AMI. Consider soldering any of them in case you experience some instability of any kind (never experienced so far).

LED1 is "run mode" indicator; it blinks at variable rates to indicate HID2AMI running status (suggesetd colors: green, yellow, white)
- When in BOOTLOADER mode, a fast blink means bootloader running and waiting for the "App" to be flashed/upgarded
- When in APP mode, a "regular" blinking means the App is running and waiting for input; a slower blinking (upon connecting a peripheral), means the peripheral correctly identified and mapped 

LED2 is the "power on" indicator; if lit then your board gets correct +5V and +3.3V power supply 

For both LED1 and LED2, the suggested value for their respective limiting current resistors is 10k, but you can safely experiment any value in range 1k-47k depending on the led components characteristics and light efficiency (and your personal taste)

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
|R13    | 100k     |   R-EU_M0805     |  M805      | MANDATORY|
|R14    | 100k     |   R-EU_M0805     |  M805      | MANDATORY|
|R15    | 100k     |   R-EU_M0805     |  M805      | MANDATORY|
|R16    | 100k     |   R-EU_M0805     |  M805      | MANDATORY|
|R17    | 100k     |   R-EU_M0805     |  M805      | MANDATORY|
|R18    | 100k     |   R-EU_M0805     |  M805      | MANDATORY|
|R19    | 100k     |   R-EU_M0805     |  M805      | MANDATORY|
|R20    | 0k       |   SHORT          |  M805      | MANDATORY|
|       |          |                  |            |          |
|U1     | F105RBT6 |   STM32F105RBT6  |  TQFP64    | MANDATORY|
|       |          |                  |            |          |
|X1     |          |   USB-CONNECTOR  |            | MANDATORY|
|X3     |          |   F09HP D-SUB9   |  F09HP     | MANDATORY|
|       |          |                  |            |          |

### **GERBER FILES**

[HID2AMI v1.0.0 DELUXE GERBER FILES](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist_2019-01-19.zip)

### **EAGLE SCHEMATICS AND BOARD LAYOUT**

[HID2AMI v1.0.0 DELUXE SCHEMATICS](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.sch)

[HID2AMI v1.0.0 DELUXE BRD](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.brd)

### **BOOTLOADER**

Current BOOTLOADER version is 1.3.0. You can freely get it from here [HID2AMIBOOTLOADER](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Firmware/HID2AMIBOOTLOADER.dfu)


### **FLASHING INSTRUCTIONS**

#### **PREREQUISITES**
In order to be able to flash both the bootloader and the HID2AMI app, you need:
- A MS-Windows PC
- An A-A USB cable (https://www.google.com/search?q=a-a+usb+cable)
- The free ST DFU Tools. Download the package from here (https://www.st.com/en/development-tools/stsw-stm32080.html)

#### **FLASHING THE BOOTLOADER**
- Install the ST DFU Tool package on your Windows machine. Make sure you have the ST DFU-USB driver installed (in case something went wrong, you can manually install them from the DFU Tool's directory)
- Set HID2AMI in DFU-BOOT mode, by selecting position 2-3 for both "BOOT0" and "PA9BOOT" jumpers
- MAKE SURE THAT HID2AMI IS NOT CONNECTED TO YOUR AMIGA MOUSE/JOY PORT
- Connect HID2AMI to any USB port of your PC, by mean of the A-A USB Cable
- After few seconds, HID2AMI should be recognized by Windows as "ST Device in DFU Mode"
- Launch "DfuSeDemo" App from ST Tools package. You should see a form like this one, showing your HID2AMI has booted in DFU mode and has been recognized properly ![DFU-BOOT](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/50-01.Dfu.Boot.jpg)
- Select the HID2AMIBOOTLOADER.dfu file you previosly downloaded from [here](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Firmware/HID2AMIBOOTLOADER.dfu) by pressing "Choose" under "Upgrade or Verify Action". 
You should come to a condition like this          ![DFU-BOOT-INJECT](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/50-02.Dfu.Bootloader.inject.jpg)
- Press "Upgrade" button and waity the process to finish with success.

#### **RETRIEVING YOUR PERSONAL BOARD CODE**
If everything went fine, your board now can boot from the BOOTLOADER and is ready to be loaded with the HID2AMI App
- Set HID2AMI in BOOTLOADER mode, by selectin position 1-2 for "BOOT0" and position 2-3 for "PA9BOOT"
- MAKE SURE THAT HID2AMI IS NOT CONNECTED TO YOUR AMIGA MOUSE/JOY PORT
- Connect HID2AMI to any USB port of your PC, by mean of the A-A USB Cable: the bootloader should take control, and you should see the activity led on board (lower led near usb connector) fastly blinking
- Look at DfuSeDemo window: you should see something like as follows. Note down the four characters you see near "Version" field ![DFU-BOOTLOADED](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/50-03.HID2AMI.Dfu.codeget.jpg)
- In order to get a properly signed app, working tied to your board, you have to ask it from the author, by sending him an [email](mailto:EmberHEavyIndustries@gmail.com) together with your personal code, which is the four character as above (in the case of the picture is "D530", yours should obviously be different)

#### **FLASHING THE HID2AMI APP**
- Once received your personalized app file, in the form "HID2AMIAPP.XXXX.dfu", boot again HID2AMI in BOOTLOADER mode (just as above), "Choose" the app file "HID2AMIAPP.XXXX.dfu" and press "Upgrade" ![DFU-LOADAPP](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/50-04.HID2AMI.Dfu.App.Inject.jpg)
- You're done ! Put the HID2AMI board in APP mode by by selecting position 1-2 for both "BOOT0" and "PA9BOOT" jumpers, **DISCONNECT you HID2AMI board from your Windows PC** and connect it to any Mouse/Joy port of your Amiga
- Enjoy !

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

## **DISTRIBUTION AND PRICING POLICY**
I've spent a great effort in designing and developing this app, so I would be grateful if you'd be happy to contibute to its future development. I decided to release all project's details, schematics and gerbers for free to everyone, but retaining myself close control over the firmware app. Being this one a no-profit hobbyist project, I can't guarantee any volume production of boards, so I will following the following distributio policies, for who may be interested in having one:

- Software only
  - You build the board yourself, by mean of the public gerbers or by a compatible custom layout you derive from schematics
  - You get the APP from me by sending me a request together with your personal 4-digits code (see instructiuons above how to get it)
  - Availability to serve request and cost of the app shall be exposed here or on the Amiga Forums I (Sampedenawa) am frequenting. Find HID2AMI on [Amigapage](http://www.amigapage.it), [EAB](https://eab.abime.net), [A1K](https://www.a1k.org). 

- DYI KIT
  - You build the board yourself by getting from me the pcb and all needed components
  - You get the APP from me by sending me a request together with your personal 4-digits code 
  - Availability and costs of DIY kits shall be exposed here or on the Amiga Forums I (Sampedenawa) am frequenting. Find HID2AMI on [Amigapage](http://www.amigapage.it), [EAB](https://eab.abime.net), [A1K](https://www.a1k.org).

- COMPLETE BOARD
  - You get the fully working board from me by sending me a request 
  - (Rare) Availability and costs of complete boards shall be exposed here or on the Amiga Forums I (Sampedenawa) am frequenting
. Find HID2AMI on [Amigapage](http://www.amigapage.it), [EAB](https://eab.abime.net), [A1K](https://www.a1k.org).

## **Warranty Disclaimer and Limitation of Liability**

HID2AMI is an hobbyist project without any commercial intention; you understand that we cannot and do not guarantee or warrant neither the HID2AMI hardware (including but not limited to: schematics, gerbers, pcb, components, assembling, etc.) nor the HID2AMI software (bootloader, app, etc) from defects, breakage or loss of functionality. You are using HID2AMI under your exclusive risk and responsibility; please understand and AGREE that **WE WILL NOT BE LIABLE FOR ANY LOSS OR DAMAGE CAUSED BY EITHER ANY USE OR ANY MISUSE OF HID2AMI**

BY MAKING USE OF HID2AMI, YOU EXPRESSLY AGREE THAT YOUR WILL ACCEPT IT ON "AS IS" BASIS WITHOUT ANY WARRANTIES OF ANY KIND, EITHER EXPRESS OR IMPLIED. YOU ALSO EXPRESSELY AGREE THAT YOUR USE OF HID2AMI HARDWARE AND ITS SOFTWARE COMPONENTS IS AT YOUR OWN RISK. NEITHER THE AUTHOR (Sampedenawa) NOR ANY PERSON ASSOCIATED WITH THE AUTHOR MAKES ANY WARRANTY OR REPRESENTATION WITH RESPECT TO THE COMPLETENESS, SECURITY, RELIABILITY, QUALITY, ACCURACY OR AVAILABILITY OF THE HID2AMI HARDWARE/SOFTWARE.

IF YOU DO NOT UNDERSTAND AND EXPRESSLY AGREE WHAT STATED ABOVE, YOU ARE NOT ENTITLED BY THE AUTHOR TO USE HID2AMI FOR ANY PURPOSE.
