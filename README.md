![HID2AMI](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HID2-AMI-Logo-Web-Show.png)

**If you like this project and want to contribute to its further development, please consider donate some $ or € (paypal friends & family, please or DO NOT select "Buying something" from money transfer frontpage).** 

Donors of at least 5 EUR will receive the latest firmware revision available at the moment of request; donors of 10 EUR or more will also be added to the "firmware beta release" channel, and will receive all intermediate beta releases and all subsequent firmware updates. Donors will also be allowed to request new features and improvements (subjet to author's discretion).

| [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/EmberHeavyIndustries)||[![Email, Contacts & Requests](https://github.com/EmberHeavyIndustries/Depot/blob/master/Pics/EmailSticker.jpg?raw=true)](mailto:EmberHEavyIndustries@gmail.com)|
| ------------------------------ | ---------------------------------------------- | --------------------------- |


[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)


**HID2AMI** is an **HID mouse to quadrature waveform converter** and **HID Gamepad adapter** for the Amiga (and C64, Atari 7600, AtariST also..) series of boards; it allows ANY modern HID mouse (not limited to PS/2-USB) and almost ANY (*) modern digital/analog Gamepad to be connected and enjoyed with our Amiga computers.

(*) At the moment it has been tested against dozens of different gamepdas,  but working for each and every existing Gamepad cannot be guaranteed; nevertheless, if you find a Pad which does not work with HID2AMI, you are encouraged to contact the author and supply him its "HID Report Descriptor" to be investigated.


[HOW TO SUBMIT AN HID DUMP ](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/hid.dump.howto.md)



## **REV 1.0 board** 
![Image of HID2AMI-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.v1.0.0-1-300.jpg) ![Image of HID2AMI-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.v1.0.0-2-300.jpg) ![Image of HID2AMI-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.Black.Top_300.jpg) ![Image of HID2AMI-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI.Black.Bottom_300.jpg)

## **REV 1.1 board** 
![Image of HID2AMI-03](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/20190321_082422_025.jpg)![Image of HID2AMI-04](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/20190321_082504_025.jpg)

## **HOW DOES IT WORK** (in brief):

HID2AMI recognizes and manages any HID device connected to its USB interface; if the device is recognized as an HID mouse, then HID2AMI starts capturing live movements and button pressings of the peripheral, then converting both of them into proper quadrature waveforms (and Amiga mouse button pressings) which can be properly understood by the Amiga itself, as if a real quadrature "Amiga" mouse was connected.

If the device is recognized as an HID gamepad, then HID2AMI maps pad's controls on the Amiga Joystick port/interface.
Gamepad's buttons are mapped evenly on Amiga button1/button2/UP/DOWN (useful for jump & racing games) inputs.
Starting from fw 1.7.1 a custom mapping can be freely configured and stored for automatic retrieval upon reconnection.

There is no need to manually configure the emulation mode: device recognition and operation mode switching are automatically performed by HID2AMI itself.

## **GETTING STARTED AND USER GUIDE**:

Here you can find a quick user guide, describing basic operations and the available meta-commands for peripheral's profile customization, storage and retrieval.

[HID2AMI QUICK USER GUIDE](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Quick.User.Guide.md)

 ## **HW AND SCHEMATICS**
  
|   Flavour      | Current ver.  |                Features               |
| -------------- | ------------- | ------------------------------------- |
| HID2AMI LITE   |    v1.0.0     |   direct output to Amiga port lines   |
| HID2AMI DeLuxe |    v1.1.0     |   output lines driven by mosfet       |
  
 
  *Two version of HID2AMI exist: Lite version (yellow) and DeLuxe version (blue/black). They are different in the way outputs to Amiga ports are buffered (DeLuxe version outputs go through mosfet buffers, for maximum compatibility with "weak" amigas).*


## **FIRMWARE**
  
|      Baseline        | Current ver.  |                Features              |
| -------------------- | ------------- | -------------------------------------|
| HID2AMI BOOTLOADER   |    v1.3.0     |   Enables DFU upgrade of APP         |
| HID2AMI APP          |    v1.8.7     |   see release notes below            |
 
 
 
 
Features of fw v1.8.7:
- Added support for Logitech MX510 MX518 G305 G203 G403 G603 G703 G903 gaming mice
- Added support for SteelSeriec Rival 110 and 600 Gaming mice
 
Features of fw v1.8.6:
- Added support for Logitech G502, G5 and G Pro Gaming mice
- Added support for SteelSeriec Rival 100, 310 and 500 Gaming mice

Features of fw v1.8.5:
- Added automatic recognition and management of hw customized report Id (improves compatibility)

Features of fw v1.8.0:
- Added support for PS3 and PS4 3rd party compatible pads 
- Added support for original Dual Shock 4 PS4 pads
- Reworked 12-bit XY axis support for gaming/precision mice
- Improved compatibility with some Logitech gaming mice

Features of fw v1.7.4:
- Added support for Logitech M560 Wireless Mouse
- 	Added support for Targus MiniMouse
- 	Added multiple HID device interface support (greatly improves compatibility)
-	Added preliminary Microsoft Wireless Laser Mouse 6000 support
- Added preliminary support to XBOX ONE gamepads

Features of fw v1.7.3:
- Added custom free mapping of first 4 buttons of Gamepad. By pressing 4buttons+LeftStickDown the board enters in mapping mode; pressing in turn single buttons maps them on Amiga1->Amiga2->Up->Down
- Added custom mapping config autosave: each custom configuration is permanently stored and recalled upon Gamepad reconnection.
- Separate permanent configs (up to 20) are saved and recalled automatically upon recognition of Gamepads brand/model
- Added support for 12 bit high resolution gaming mice
- Added customizable real-time mouse pointer speed adjust, by rolling the mousewheel forward/backwards
- Added save of permanent config for mouse pointer speed, by pressing L-M-R buttons together 

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



## **READ CAREFULLY BEFORE CONNECTING ANY PAD/MOUSE TO YOUR AMIGA**

 **BE AWARE** that when you connect a peripheral to the Amiga's mouse/joy port, the power supply or that peripheral comes from/through that port itself. **Be aware that improperly connecting an "high" power-demanding device could lead to overheat or even damage the Amiga joy/mouse port**. 

If you connect controllers with rechargeable batteries, **be absolutely confident that the battery has been fully charged**  **BEFORE** connecting it to the Amiga, or the charging current flowing from the joy/mouse port to your controller's battery could seriosly damage your Commodore  !

 You are usign HID2AMI at your own risk: I will either not be liable nor responsible for any damage you could cause to your hardware for any use or misuse of HID2AMI together with your systems.  





## **COMPATIBILITY LIST**

(!) HID2AMI has been tested against a number of HID compliant Mice and Gamepads; the following compatibility list keeps track of tested peripherals. If you tested your mice/Gamepads and want to contribute to the list, simply send an email to the author with your compatibility results. In case your device is not handled properly, you ca submit the author an HID dump to be investigated.  
[HOW TO SUBMIT AN HID DUMP ](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/hid.dump.howto.md)

Thanks !


|      Device      |                Model               | Min required fw ver. | Working |                Notes                 |     |
| ---------------- | ---------------------------------  |----------- | ------- | -------------------------------------| --- |
| Mice             | Any HID Compliant Mouse            |  v1.0.0    |  YES    | Any HID mouse                        |![MOU1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HID.HP.Mouse_200.jpg)|
| Mouse            | Logitech G5   Gaming Mouse         |  v1.8.6    |  YES    |                                      |![MOU7](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.G5_200.jpg)|
| Mouse            | Logitech G502 Gaming Mouse         |  v1.8.6    |  YES    |                                      |![MOU6](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.G502_200.jpg)|
| Mouse            | Logitech G Pro Gaming Mouse        |  v1.8.6    |  YES    |                                      |![MOU8](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.GPro_200.jpg)|
| Mouse            | Logitech MX510 MX518 G305 G203 G403 G603 G703 G903 RX250       |  v1.8.7    |  YES    |                                      |![MOUD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.logitech.gmice_200.jpg)|
| Mouse            | Logitech Wireless Mouse M220, M560    |  v1.7.4    |  YES    |                                      |![MOU3](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.M560_200.jpg)|
| Mouse            | Logitech Wireless Mouse M590       |  v1.8.4    |  YES    |                                      |![MOU4](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.M590_200.jpg)|
| Mouse            | Logitech Wireless Mouse Mx Master  |  v1.8.4    |  YES    |                                      |![MOUD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.logitech-mx-master_200.jpg)|
| Mouse            | Microsoft Intellimouse             |  v1.6.0    |  YES    | Not 100% HID protocol compliant      |![MOU2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Intellimouse_200.jpg)|
| Mouse            | Microsoft Intellimouse Explorer    |  v1.8.4    |  YES    | Wireless explorer series             |![MOU5](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Microsoft.Intellimouse.Explorer_200.jpg)|
| Mouse            | Microsoft Wireless Laser Mouse 6000|  v1.8.4    |  YES    | Wireless explorer series             |![MOUD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.MS.Laser.mouse.6000_200.jpg)|
| Mouse            | Rapoo 7100P  Wireless Mouse        |  v1.8.6    |  YES    |                                      |![MOUE](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Rapoo.Wireless_200.jpg)|
| Mouse            | Steelseries Rival 100 and 110      |  v1.8.6    |  YES    |                                      |![MOU9](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Steelseries.Rival.100_200.jpg)|
| Mouse            | Steelseries Rival 310              |  v1.8.6    |  YES    |                                      |![MOUA](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Steelseries.Rival.310_200.jpg)|
| Mouse            | Steelseries Rival 500              |  v1.8.6    |  YES    |                                      |![MOUB](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Steelseries.Rival.500_200.jpg)|
| Mouse            | Steelseries Rival 600              |  v1.8.7    |  YES    |                                      |![MOUC](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Steelseries.Rival.600_200.jpg)|
| Mouse            | Targus Mini Mouse                  |  v1.7.4    |  YES    | Not 100% HID protocol compliant      |![MOU4](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Targus.Mouse.Mini_200.jpg)|
| Joystick         | Arcade Stick w/ USB encoder        |  v1.3.0    |  YES    | Stick is digital only                |![ARC1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Arcade.stick_200.jpg)|
| Joystick         | C64 Mini Stick                     |  v1.3.0    |  YES    | Stick is digital only                |![C641](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Joystick.C64.Mini_200.jpg)|
| Gamepad          | Dual Stick China Clone             |  v1.3.0    |  YES    | Both digital and analog mode         |![CHN1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.DualStick.Chinese_200.jpg)|
| Gamepad          | Dual Wireless PS3-USB              |  v1.8.0    |  YES    | Both digital and analog mode         |![CHN2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Dual.Wireless.PS2.jpg)|
| Gamepad          | Hama Whitestorm                    |  v1.3.0    |  YES    | Both digital and analog mode         |![HAM1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HAMA_200.jpg)|
| Joystick         | HORI FightingStick Mini            |  v1.8.0    |  YES    | Both PS3 and PS4 mode                |![HFS1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HORI.FightingStick_200.jpg)|
| Gamepad          | Logitech PS2 Wireless              |  v1.3.0    |  YES    | Both digital and analog mode         |![WPS2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.PS2.Wireless_200.jpg)|
| Gamepad          | Logitech Rumble Gamepad F310       |  v1.6.0    |  YES    | Both PC and XBOX 360 mode            |![WRP5](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.F310_200.jpg)|
| Gamepad          | Logitech Rumble Gamepad F510       |  v1.6.0    |  YES    | Both PC and XBOX 360 mode            |![WRP3](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.Rumble.Gamepad.F510_200.jpg)|
| Gamepad          | Logitech Rumblepad 2               |  v1.3.0    |  YES    | Both digital and analog mode         |![WRP1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.RumblePad2_200.jpg)|
| Gamepad          | Logitech Wingman Rumblepad         |  v1.3.0    |  YES    | Both digital and analog mode         |![WRP2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Wingman.Rumblepad_200.jpg)|
| Gamepad          | Logitech Wireless Gamepad F710     |  v1.8.0    |  YES    | Both PC and XBOX 360 mode            |![WRP4](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.Wireless.Gamepad.F710_200.jpg)|
| Gamepad          | PS3/PC Clones                      |  v1.5.2    |  YES    | Both digital and analog mode         |![PS3CLONE](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.PS3.Clone_200.jpg)|
| Gamepad          | RetroLink Classic Controller USB   |  v1.8.0    |  YES    | (Sega Saturn Style)                  |![SEGASAT](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.retrolink.classic_200.jpg)|
| Joystick         | SEGA VirtuaStick High Grade        |  v1.8.0    |  YES    | PS3 mode - Stick is digital only     |![SEG1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.VirtuaStickHighGrade_200.jpg)|
| Gamepad          | Sony PS1 original pad              |  v1.6.0    |  YES    | With USB adapter                     |![THFS3](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Sony.PS1.PAD_200.jpg)|
| Gamepad          | Sony PS2 original pad              |  v1.6.0    |  YES    | With USB adapter                     |![THFS5](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Sony.PS2_200.jpg)|
| Gamepad          | Sony PS2 original pad              |  v1.8.1    |  YES    | With DUAL USB adapter (1)            |![THFS7](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.PS2.Dual.Adaptor.jpg)|
| Gamepad          | Sony PS-ONE original pad           |  v1.6.0    |  YES    | With USB adapter                     |![THFS6](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Sony.PSONE.PAD_200.jpg)|
| Gamepad          | Sony Dual Shock 4 PS4 original pad |  v1.8.0    |  YES    | **WARNING !! (2)**                   |![SDS4](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.SONY.DS4.ORIGINAL_200.jpg)|
| Gamepad          | SNES Usb Clone                     |  v1.3.0    |  YES    | Pad is digital only                  |![THFS4](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.SNES.CLONE_200.jpg)|
| Joystick         | Speedlink Competition PRO USB      |  v1.8.0    |  YES    |                                      |![SLNK1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.SPEEDLINK_200.jpg)|
| Gamepad          | Thrustmaster Firestorm Digital     |  v1.3.0    |  YES    | Pad is digital only                  |![THFS2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Thrustmaster.Firestorm_200.jpg)|
| Gamepad          | Thrustmaster Wireless dual trigger |  v1.3.0    |  YES    | Both digital and analog mode         |![THWD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Thrustmaster.Wireless_200.jpg)|
| Gamepad          | XBOX 360 Clone                     |  v1.6.0    |  YES    | Not HID protocol compliant           |![XBOX](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.XBOX.360_200.jpg) 
| Gamepad          | XBOX Elite                         |  future    |  NO     | Not HID protocol compliant           |![XBOXE](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.XBOX.Elite_200.jpeg)
 
 (1) Plug the pad in adaptor #1 port
 
 (2) **WARNING! If using the wired version, either remove internal battery (suggested) or be sure it is 100% charged before connecting to your Amiga**
 
## **DEVELOPMENT**

HID2AMI hardware and firmware were designed, developed and maintained by **Sampedenawa** on behalf of **EmberHeavyIndustries** (an evil worldwide company, whose mission is to rule the world by the mean of reviving Amiga computers), following a discussion born on Italian www.amigapage.it Amiga forum.


## **ASSEMBLY**

 ## **WARNING !!  A COUPLE THINGS YOU MUST UNDERSTAND BEFORE GOING FURTHER**
 
 - **NEVER, NEVER, NEVER connect "both sides" of HID2AMI to a power source at the same time !**
 **This means: do not connect HID2AMI to a PC through the USB port while it is plugged into your Amiga's joy/mouse port !**
 **If you want to upgrade your HID2AMI with bootloader or DFU mode, beware to disconnect it from your Amiga first !**
 
 - **BE AWARE** that when you connect a peripheral to the Amiga's mouse/joy port, the power supply or that peripheral comes from/through that port itself. Amiga control peripheral ports were probably not designed with "mega-rumble-end-of-universe-nuclear-powered" gamepads in mind: while there is generally no risk in connecting "common" mainstream peripherals like the ones have been tested (see above), be aware that improperly connecting an "high" power-demanding device could lead to overheat or even damage the Amiga joy/mouse port. **You can consider the power consumption safety limit roughly around 100mA; exceeding this limit could be dangerous for your Amiga!.** 
 
 ## **You are usign HID2AMI at your own risk: I will either not be liable nor responsible for any damage you could cause to your hardware for any use or misuse of HID2AMI together with your systems.**  
 


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

[HID2AMI v1.0.0 SCHEMATICS SHEET](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.sch)

[HID2AMI v1.1.0 SCHEMATICS SHEET](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.redist.sch)

#### **REFERENCE LAYOUTS**

[Reference Layout v1.0.0 Top](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.layout.top.pdf)

[Reference Layout v1.0.0 Bottom](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.layout.bottom.pdf)

[Reference Layout v1.1.0 Top](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.layout.top.pdf)

[Reference Layout v1.1.0 Bottom](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.layout.bottom.pdf)

#### **BILL OF MATERIALS**

Components noted as "Optional" fulfil the general purpose STM32F1x reference design; generally speaking they can be safely omitted from the assembly of HID2AMI. Consider soldering any of them in case you experience some instability of any kind (never experienced so far).

LED1 is "run mode" indicator; it blinks at variable rates to indicate HID2AMI running status (suggesetd colors: green, yellow, white)
- When in BOOTLOADER mode, a fast blink means bootloader running and waiting for the "App" to be flashed/upgraded
- When in APP mode, a "regular" blinking means the App is running and waiting for input; a slower blinking (upon connecting a peripheral), means the peripheral correctly identified and mapped 

LED2 is the "power on" indicator; if lit then your board gets correct +5V and +3.3V power supply 

For both LED1 and LED2, the suggested value for their respective limiting current resistors is 10k, but you can safely experiment any value in range 1k-47k depending on the led components characteristics and light efficiency (and your personal taste)

[Reference BOM v1.0.0](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.BOM.txt)

[Reference BOM v1.1.0](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.BOM.txt)


### **GERBER FILES**

[HID2AMI v1.0.0 DELUXE GERBER FILES](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist_2019-01-19.zip)

[HID2AMI v1.1.0 DELUXE GERBER FILES](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.redist_2019-02-28.zip)

### **EAGLE SCHEMATICS AND BOARD LAYOUT**

[HID2AMI v1.0.0 DELUXE SCHEMATICS](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.sch)

[HID2AMI v1.0.0 DELUXE BRD](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.brd)

[HID2AMI v1.1.0 DELUXE SCHEMATICS](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.redist.sch)

[HID2AMI v1.1.0 DELUXE BRD](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.redist.brd)

### **BOOTLOADER**

Current BOOTLOADER version is 1.3.0. You can freely get it from here [HID2AMIBOOTLOADER](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Firmware/HID2AMIBOOTLOADER.dfu)


### **FLASHING INSTRUCTIONS**

Detailed flashing instructions, and how to get your personal HID2AMI board code, can be found here, for both Linux (courtesy by Sukkopera) and Windows:

[HID2AMI FLASHING INSTRUCTIONS](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Flashing.Instructions.md)


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
