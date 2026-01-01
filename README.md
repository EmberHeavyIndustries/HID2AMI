![HID2AMI](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HID2-AMI-Logo-Web-Show.png)


## ** Preassembled units **: If you are interested in ready-to-go pre-assembled units, a small number of them is available from time to time, assembled by various users/hobbyists. You can look for one on Amibay's thread [link] and check if there is any available on sale (https://www.amibay.com/threads/new-hid2ami-v3-1-0-mousewheel-support-personality-switch-hid-mouse-and-gamepad-to-amiga-adaptor.2451017/) 

|||[![Email, Contacts & Requests](https://github.com/EmberHeavyIndustries/Depot/blob/master/Pics/EmailSticker.jpg?raw=true)](mailto:EmberHEavyIndustries@gmail.com)|
| ------------------------------ | ---------------------------------------------- | --------------------------- |


[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)


**HID2AMI** is an **HID mouse to quadrature waveform converter** and **HID Gamepad adapter** for the Amiga (and C64, Atari 7600, AtariST also..) series of boards; it allows ANY modern HID mouse (not limited to PS/2-USB) and almost ANY (*) modern digital/analog Gamepad to be connected and enjoyed with our Amiga computers.

(*) At the moment it has been tested against dozens of different gamepads,  but working for each and every existing Gamepad cannot be guaranteed; nevertheless, if you find a Pad which does not work with HID2AMI, you are encouraged to contact the author and supply him its "HID Report Descriptor" to be investigated.


[HOW TO SUBMIT AN HID DUMP ](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/hid.dump.howto.md)

## **ENABLING MOUSEWHEEL SUPPORT**

In order the mousewheel events to be recognized from Amiga side, a proper driver has to be installed on Amiga.

The driver is freely available, and can be downloaded from the FIRMWARE folder on this github
![DRIVER](https://github.com/EmberHeavyIndustries/HID2AMI/blob/faf72c40f998a1fadbb46edbc19f1a4def65b4c7/Firmware/Hid2Ami.lha)

## **REV 3.1 board** 

HID2AMI Rev. 3.1 board (released in February 2025) upgrades previous versions by compacting the size and layout to the tiniest possible, plus adding the capability to switch firmware functions on the fly.

Rev. 3.1.0 comes with the new fromware v4.0.0 which adds the capability to switch among AMIGA - ATARI_ST - C64 behavior, with peculiar features for each.
All V4.x series firmwares will be backward compatible with V2 and V1 boards

![Image of HID2AMIV3-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/V3_01.jpg)
![Image of HID2AMIV3-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/V3_02.jpg)
![Image of HID2AMIV3-03](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/V3_03.jpg)

|      Personality      |  Switch position 0     1     2             | Notes                                              |
| --------------------- | --------------------------------- |--------------------------------------------------- |
| Amiga                 |         OFF   OFF   OFF           | Default Classic HID2AMI                            | 
| Atari ST              |         ON    OFF   OFF           | ST Mouse and Joystick/Joypad                       |
| C64                   |         OFF   ON    OFF           | C64 Joystick/Joypad with 2nd button                |


## **Lemaru's shell case (Rev 3.x boards only)** 

Thanks to the talented friend Lemaru, an awesome cover is available for everyone.

You are free to download the stl/step files linked below, and print your own copy of this awesome accessory !

![Image of EBOX30-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Sheel30_00s.jpg)
![Image of EBOX30-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Sheel30_01s.jpg)
![Image of EBOX30-03](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Sheel30_02s.jpg)
![Image of EBOX30-04](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Sheel30_03s.jpg)

[ShellBox30 Top](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/HID2AmiV3_Base.stl)

[Shellbox30 Bottom](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/HID2AmiV3_Lid.stl)


## **REV 2.0 board** 

HID2AMI Rev. 2.0 board (released in Autumn 2022) upgrades previous versions by adding capability of supporting Mousewheel and CD32 protocols, in a smaller compact shape.

Current firmware v3.0.0 act in the very same way of v1.x.x, with Mousewheel support (CD32 support  will be added in future releases)

![Image of HID2AMI-06](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMIv2.jpg)!
![Image of EBOX20-04](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/resin_1s.jpg)!
![Image of EBOX20-04](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/resin_2s.jpg)!

(Transparent shellcase images courtesy by IAmAddict)

## **NEW v3.0.0 FIRMWARE WITH MOUSEWHEEL SUPPORT** 

Starting from v3.0.0 firmware, support for mousewheel to ANY adapter hw revision (v1.0, v1.1, V2.0) has been added.

The firmware can be directly flashed on all revisions, and enables native Mousewheel support in v2.0.

In order to enable Mousewheel support on v1.x revisions, a couple of little hacks must be performed on the boards.
The hacks to be performed are: 
- short two adiacent pins of the STM32 microprocessr, by mean of a tiny drop of solder alloy (see pic)
- remove Q2 mosfet and shorten two of the pads (see pic)

![HACK01](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/HID2AMI_MW_HACK_01small.jpg)
![HACK02](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/HID2AMI_MW_HACK_02small.jpg)

After the mod, mousewheel works in v1.x all the same way it works in v2.0.
Though the mod is quite trivial, it need a minimal soldering experience.
I cannot be held responsible if anybody damages his board(s) while not properly performing the mod.

In order the mousewheel events to be recognized from Amiga side, a proper driver has to be installed on Amiga.

The driver is freely available, and can be downloaded from the FIRMWARE folder on this github
![DRIVER](https://github.com/EmberHeavyIndustries/HID2AMI/blob/faf72c40f998a1fadbb46edbc19f1a4def65b4c7/Firmware/Hid2Ami.lha)

## **REV 1.1 board** 
![Image of HID2AMI-03](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/aa.01.jpg)![Image of HID2AMI-04](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/aa.02.jpg)![Image of HID2AMI-05](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/aa.03.jpg)

## **Ember Heavy Industries's official Open source shell case (Rev 2.x boards only)** 

You are free to download the stl/step files linked below, and print your own copy of this beautiful shell cover !

![Image of EBOX20-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Shell_20_01s.jpg)
![Image of EBOX20-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Shell_20_02s.jpg)
![Image of EBOX20-03](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Shell_20_03s.jpg)

![Image of EBOX20-03](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Shell_20_04s.jpg)

(Sample 3D print by Solaris104)

![Image of EBOX20-04](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/resin_1s.jpg)
![Image of EBOX20-05](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/resin_2s.jpg)
![Image of EBOX20-06](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/resin_3s.jpg)

(Sample 3D print by IAmAddicted)

[ShellBox Top](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/HID2AMI_ShellUpper.stl)

[Shellbox Bottom](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/HID2AMI_ShellLower.stl)


## **CERV's free shell case (Rev 2.x boards only)** 

User Cerv kindly designed and shared his alternative box design !

![Image of EBOX20-06](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/HID2AMI_BOX_CERV.jpg)


[ShellBox Cover](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/HID2AMI_CERV_cover.stl)

[Shellbox Case](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/HID2AMI_CERV_box.stl)



## **Ember Heavy Industries's official Open source shell case (Rev 1.1 boards only)** 

#### Based upon Lemaru's shell, with some enhancements and eye-catching HID2AMI logo carved on top  !

You are free to download the stl/step files linked below, and print your own copy of this beautiful shell cover !

![Image of EBOX-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/88.HID2AMI_SHELL_EMBER_00.jpg)
![Image of EBOX-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/88.HID2AMI_SHELL_EMBER_01.jpg)
![Image of EBOX-03](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/88.HID2AMI_SHELL_EMBER_02.jpg)
![Image of EBOX-04](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/88.HID2AMI_SHELL_EMBER_03.jpg)

[ShellBox Top](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/88.EmberHID2AMI.UpperShell_1.stl)

[Shellbox Bottom](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/88.EmberHID2AMI.LowerShell_1.stl)



## **GothDevil's Open source shell case (Rev 1.1 boards only)** 

#### Thanks to the talented and friendly user **GothDevil** for creating and sharing her precious work  !

You are free to download the stl/step files linked below, and print your own copy of this beautiful shell cover !

![Image of BOX-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/77.BOX_01_50.jpg)![Image of BOX-02](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/77.BOX_02_50.jpg)![Image of BOX-03](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/77.BOX_03_50_2.jpg)


[ShellBox Top](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/top_cover_final.stl)

[Shellbox Bottom](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/bottom_cover_final.stl)


#### GothDevil kindly allows free and open distribution of this excellent work; nevertheless I (EmberHeavyIndustries) would consider it fair if anyone who enjoys her effort would give her a little donation (say: 1 EUR) to thank her for sharing.
Please send donations to GothDevil's paypal account here:


| [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/HID2AMIBOX)||Thank you GothDevil !|
| ------------------------------ | ---------------------------------------------- | --------------------------- |

## **Lemaru's Open source shell case (Rev 1.1 boards only)** 

#### Thanks to the talented and friendly user **Lemaru** for creating and sharing his precious work  !
!

You are free to download the stl/step files linked below, and print your own copy of this beautiful shell cover !

![Image of BOX-01](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/77.Lemaru_shell_350.jpg)


[ShellBox Top](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/HID2AMI_Top.stl)

[Shellbox Bottom](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/HID2AMI_Bottom.stl)



## **HOW DOES IT WORK** (in brief):

HID2AMI recognizes and manages any HID device connected to its USB interface; if the device is recognized as an HID mouse, then HID2AMI starts capturing live movements and button pressings of the peripheral, then converting both of them into proper quadrature waveforms (and Amiga mouse button pressings) which can be properly understood by the Amiga itself, as if a real quadrature "Amiga" mouse was connected.

If the device is recognized as an HID gamepad, then HID2AMI maps pad's controls on the Amiga Joystick port/interface.
Gamepad's buttons are mapped evenly on Amiga button1/button2/UP/DOWN (useful for jump & racing games) inputs.
Starting from fw 1.7.1 a custom mapping can be freely configured and stored for automatic retrieval upon reconnection.

There is no need to manually configure the emulation mode: device recognition and operation mode switching are automatically performed by HID2AMI itself.

## **GETTING STARTED AND USER GUIDE**:

Here you can find a quick user guide, describing basic operations and the available meta-commands for peripheral's profile customization, storage and retrieval.

[HID2AMI QUICK USER GUIDE](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Quick.User.Guide.md)




## **COMPATIBILITY LIST**

(!) HID2AMI has been tested against a number of HID compliant Mice and Gamepads; the following compatibility list keeps track of tested peripherals. If you tested your mice/Gamepads and want to contribute to the list, simply send an email to the author with your compatibility results. In case your device is not handled properly, you can submit an HID dump to the author for investigation.  
[HOW TO SUBMIT AN HID DUMP ](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/hid.dump.howto.md)

Thanks !


|      Device      |                Model               | Min required fw ver. | Working |                Notes                 |     |
| ---------------- | ---------------------------------  |----------- | ------- | -------------------------------------| --- |
| Mice             | Any HID Compliant Mouse            |  v1.0.0    |  YES    | Any HID mouse                        |![MOU1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HID.HP.Mouse_200.jpg)|
| Mouse            | New USB Tank Mouse                 |  v1.0.0    |  YES    |                                      |![MOU66](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.HID.HP.TANK_200.jpg)|
| Mouse            | Anker Ergonomic Vertical Mouse     |  v1.8.4    |  YES    |                                      |![ANKERA](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Anker_Ergonomic_200.jpg)|
| Mouse            | Labtec Optical Mouse 600           |  v1.8.4    |  YES    |                                      |![MOULA](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Labtec.Optica.Mouse.600_200.jpg)|
| Mouse            | Logitech B100                      |  v1.0.0    |  YES    |                                      |![MOUF](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.B100_200.jpg)|
| Mouse            | Logitech M570                      |  v1.0.0    |  YES    |                                      |![MOUF570](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/m570.jpg)|
| Mouse            | Logitech G5   Gaming Mouse         |  v1.8.6    |  YES    |                                      |![MOU7](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.G5_200.jpg)|
| Mouse            | Logitech G502 Gaming Mouse         |  v1.8.6    |  YES    |                                      |![MOU6](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.G502_200.jpg)|
| Mouse            | Logitech G Pro Gaming Mouse        |  v1.8.6    |  YES    |                                      |![MOU8](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.GPro_200.jpg)|
| Mouse            | Logitech MX510 MX518 G305 G203 G300 G40X G603 G70X G903 RX250     |  v1.8.7    |  YES    |     |![MOUD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.logitech.gmice_200.jpg)|
| Mouse            | Logitech M-BT83 Wired Mouse        |  v1.9.2    |  YES    |                                      |![MOULO2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.M-BT83_200.jpg)|
| Mouse            | Logitech Performance MX BT         |  v1.8.7    |  YES    |                                      |![MOU10](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.Performance.MX_200.jpg)|
| Mouse            | Logitech Wireless Mouse M220, M305, M560, M70X    |  v1.7.4    |  YES    |                             |![MOU3](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.M560_200.jpg)|
| Mouse            | Logitech Wireless Mouse M590       |  v1.8.4    |  YES    |                                      |![MOU4](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Logitech.M590_200.jpg)|
| Mouse            | Logitech Wireless Mouse Mx Master  |  v1.8.4    |  YES    |                                      |![MOUD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.logitech-mx-master_200.jpg)|
| Mouse            | Microsoft Classic Intellimouse 2018|  v1.8.c    |  YES    |                                      |![MOUCL](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Microsoft.Classic.Intellimouse_200.jpg)| 
| Mouse            | Microsoft Intellimouse             |  v1.6.0    |  YES    | Not 100% HID protocol compliant      |![MOU2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Intellimouse_200.jpg)| 
| Mouse            | Microsoft Intellimouse Explorer    |  v1.8.4    |  YES    | Wireless explorer series             |![MOU5](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Microsoft.Intellimouse.Explorer_200.jpg)|
| Mouse            | Microsoft Wireless Laser 6000, 7000|  v1.8.4    |  YES    | Wireless explorer series             |![MOUD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.MS.Laser.mouse.6000_200.jpg)|
| Mouse            | Rapoo 7100P  Wireless Mouse        |  v1.8.6    |  YES    |                                      |![MOUE](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Rapoo.Wireless_200.jpg)|
| Mouse            | Steelseries Rival 100 and 110      |  v1.8.6    |  YES    |                                      |![MOU9](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Steelseries.Rival.100_200.jpg)|
| Mouse            | Steelseries Rival 310              |  v1.8.6    |  YES    |                                      |![MOUA](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Steelseries.Rival.310_200.jpg)|
| Mouse            | Steelseries Rival 500              |  v1.8.6    |  YES    |                                      |![MOUB](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Steelseries.Rival.500_200.jpg)|
| Mouse            | Steelseries Rival 600              |  v1.8.7    |  YES    |                                      |![MOUC](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Steelseries.Rival.600_200.jpg)|
| Mouse            | Targus Mini Mouse                  |  v1.7.4    |  YES    | Not 100% HID protocol compliant      |![MOU4](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Targus.Mouse.Mini_200.jpg)|
| Mouse            | Trust Wireless 18519 YVI           |  v1.8.8    |  YES    |                                      |![MOU11](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Trust.18519.Wireless_200.jpg)|
| Mouse            | Yenkee YMS 3007                    |  v1.8.4    |  YES    |                                      |![MOULY](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Yenkee.yms.3007_200.jpg)|
| Gamepad          | 8bitd0 SFC30 Bluetooth             |  v1.8.0    |  YES    |                                      |![(BITD=](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.8bitdo.200.jpg)|
| Gamepad          | 8bitd0 M30 Wireless 2.4G           |  v1.8.0    |  YES    |                                      |![(BITE=](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/8BitDo.jpg)|
| Adapter          | 8bitd0 Wireless adapter 2.4G       |  v1.8.0    |  YES    | All wireless controllers (xbox ONE, etc) |![(BITF=](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.8bitdo.jpg)|
| Joystick         | Arcade Stick w/ USB encoder        |  v1.3.0    |  YES    | Stick is digital only                |![ARC1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Arcade.stick_200.jpg)|
| Joystick         | C64 Mini Stick                     |  v1.3.0    |  YES    | Stick is digital only                |![C641](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Joystick.C64.Mini_200.jpg)|
| Gamepad          | Diswoe Wireless PC/Nintendo Switch |  v1.8.0    |  YES    |                                      |![(DISW=](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/Diswoe_Wireless.jpg)|
| Gamepad          | Dual Stick China Clone             |  v1.3.0    |  YES    | Both digital and analog mode         |![CHN1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.DualStick.Chinese_200.jpg)|
| Gamepad          | Dual Wireless PS3-USB or BT        |  v1.9.8    |  YES    | Both digital and analog mode  (3)    |![CHN2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Dual.Wireless.PS2.jpg)|
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
| Gamepad          | SEGA Mega Drive Mini USB Pad       |  v1.9.1    |  YES    |                                      |![SEG2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.sega_mega_drive_mini.jpg)|
| Joystick         | SEGA VirtuaStick High Grade        |  v1.8.0    |  YES    | PS3 mode - Stick is digital only     |![SEG1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.VirtuaStickHighGrade_200.jpg)|
| Gamepad          | Sony PS1 original pad              |  v1.6.0    |  YES    | With USB adapter                     |![THFS3](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Sony.PS1.PAD_200.jpg)|
| Gamepad          | Sony PS2 original pad              |  v1.6.0    |  YES    | With USB adapter                     |![THFS5](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Sony.PS2_200.jpg)|
| Gamepad          | Sony PS2 original pad              |  v1.8.1    |  YES    | With DUAL USB adapter (1)            |![THFS7](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.PS2.Dual.Adaptor.jpg)|
| Gamepad          | Sony PS-ONE original pad           |  v1.6.0    |  YES    | With USB adapter                     |![THFS6](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Sony.PSONE.PAD_200.jpg)|
| Gamepad          | Sony Dual Shock 3 PS3 original pad |  v1.8.b    |  YES    | With USB cable or BT **WARNING !! (2) (3)**  |![SDS5](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/66.PS3.Dualshock3_200.jpg)|
| Gamepad          | Sony Dual Shock 4 PS4 original pad |  v1.8.0    |  YES    | **WARNING !! (2)**                   |![SDS4](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.SONY.DS4.ORIGINAL_200.jpg)|
| Gamepad          | SNES Usb Clone                     |  v1.3.0    |  YES    | Pad is digital only                  |![THFS4](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.SNES.CLONE_200.jpg)|
| Joystick         | Speedlink Competition PRO USB      |  v1.8.0    |  YES    |                                      |![SLNK1](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.SPEEDLINK_200.jpg)|
| Gamepad          | Thrustmaster Firestorm Digital     |  v1.3.0    |  YES    | Pad is digital only                  |![THFS2](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Thrustmaster.Firestorm_200.jpg)|
| Joystick         | Thrustmaster T-16000M              |  v1.8.0    |  YES    |                                      |![(THT16=](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/Threstmaster_T-16000M.jpg)|
| Gamepad          | Thrustmaster Wireless dual trigger |  v1.3.0    |  YES    | Both digital and analog mode         |![THWD](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.Thrustmaster.Wireless_200.jpg)|
| Gamepad          | XBOX 360 Clone                     |  v1.6.0    |  YES    | Not HID protocol compliant           |![XBOX](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.XBOX.360_200.jpg) 
| Gamepad          | XBOX Elite                         |  v1.8.0    |  YES (*) |(*) works via 8bitdo Wireless dongle |![XBOXE](https://raw.githubusercontent.com/EmberHeavyIndustries/HID2AMI/master/Pics/66.XBOX.Elite_200.jpeg)
 
 (1) Plug the pad in adaptor #1 port
 
 (2) **WARNING! If using the wired version, either remove internal battery (suggested) or be sure it is 100% charged before connecting to your Amiga**
 
 (3) Click d-pad (Hat) soon after connection to start auto-reconfiguration of the pad

 ## **HW AND SCHEMATICS**
  
|   Flavour      | Current ver.  |                Features               |
| -------------- | ------------- | ------------------------------------- |
| HID2AMI LITE   |    v1.0.0     |   direct output to Amiga port lines   |
| HID2AMI DeLuxe |    v1.1.0     |   output lines driven by mosfet       |
| HID2AMI DeLuxe |    v2.0.0     |   compact size, reduced mosfets       |
  
 


## **FIRMWARE**
  
|      Baseline        		| Current ver.  |                Features              |
| -------------------- 		| ------------- | -------------------------------------|
| HID2AMI BOOTLOADER   		|    v1.4.0     |   Enables DFU upgrade of APP         |
| HID2AMI OEM BOOTLOADER   	|    v1.4.0     |   Enables DFU upgrade of APP         |
| HID2AMI APP          		|    v4.0.3   	|   see release notes below            |


Features of fw v4.03
 - Added customizable keyboard mapping (SWOS edition)
 - Fixed C64 mode keyb conflict
 - Fixed Mouse scroll down not working in some A1200

Features of fw v4.0.2
-	SWOS edition
-	Enabled USB keyboard support

Features of fw v4.0.1
 - 	Added Razer Steel Series Rival 3 Mouse support

Features of fw v4.0.0
 - 	HRW v3.x support - full backward compatibility with v2.x and v1.x (v1.x need scrollwheel hw hack)
 - 	HRW v3.x personality mode switch AMIGA-ATARI-C64
   
|      Personality      |  Switch position 0     1     2             | Notes                                              |
| --------------------- | --------------------------------- |--------------------------------------------------- |
| Amiga                 |         OFF   OFF   OFF           | Default Classic HID2AMI                            | 
| Atari ST              |         ON    OFF   OFF           | ST Mouse and Joystick/Joypad                       |
| C64                   |         OFF   ON    OFF           | C64 Joystick/Joypad with 2nd button                |

Features of fw v3.0.5
 - 	Added flash storage for PS4 controllers mapping
 - 	Added Logitech VX Nano support
 - 	Added Logitech G403 Hero support
 - 	Added Advanced Corded Mouse M500s support
 - 	All Logitech wireless dongles default to mouse

Features of fw v3.0.4
 - Fixed an elusive bug that activated the multiplier setup mode each time the power was turned back on
 - Fixed a bug where changing mouse pointer direction after a stop. Mouse movements are now pixel perfect

Features of fw v3.0.3
 - Maintenance release
   
Features of fw v3.0.2
 - Added support for Logitech G602, G9x, G700
 - Added support for Razer DeathAdder 2013
 - Added support for Dell Wireless Mouse (from set KM3322W)
 - Added support for X8 mouse speed demultiplier (1000dpi + mice)
 - Added support for "Mad Catz" Speedlink competition pro

Features of fw v3.0.1
 - Enabled management of 3rd mouse button in conjunction with MouseWheel
 
Features of fw v3.0.0
 - Unified firmware for all HID2Ami revisions, compatible with v1.0, v1.1, v2.0
 - Add mousewheel support on all Amigas (V2.0)
 - Add mousewheel support with v1.x boards + hw fix
 
Features of fw v1.9.8
 - Added support for Microsoft Wireless Mobile Mouse 4000
 - Added support for Logitech MX Revolution Mouse
 - Added support for Logitecg G400 Gaming Mouse
 - Added support for Logitech G700 Laser Mouse
 - Added support for Logitexh MX Master 3S
 - Added support for PS3 DualShock3 BT adapter plus coded trick to detect USB o BT connection (move hat soon after connecting)
 - Fixed deadzone values for XBOX360 pads

Features of fw v1.9.7:
 - Added full mapping support for XBox360 and compatible pads
 
Features of fw v1.9.6:
 - Added support for cursor arrow keys in keyboard driver
 - Joypad buttons now can be mapped either B1-B2-UP-DN or B1-B2-B1-B2 (the latter by pressing LEFT direction while mapping) 
 - Added MS Touch Wireless Mouse support
 - Added MS BTechnology wireless adapter
 - Fixed a custom HID mouse protocol init bug (greatly improves compatiiblity with non standard HID devices) 

Features of fw v1.9.5:
 - Added support for Logitech B170 / M170 wireless adapters and peripherals
 - Added generic support for composite (multi-peripheral) Logitech devices
	
Features of fw v1.9.4:
 - Fixed a very stupid bug, which caused quadrature waveform emulation non behaving correctly.
        Though anybody noticed it (not even myself until now !), the fixed quadrature waveform now performs
        way smoother pointer movements. 
	
Features of fw v1.9.3:
  - Added support for SpeedLink Competition Pro USB 2019+
  - Fixed a stupid bug not clearing device mapping upon disconnection (very hardly to occur, indeed)
 
Features of fw v1.9.2:
  - Added support for Logitech M-BT83 Wired Mouse 
   
Features of fw v1.9.1:
  - Added support for SEGA Mega Drive Mini USB Adapters 

Features of fw v1.9.0:
  - Added support for HID keyboards with "WADS" mapping 

Features of fw v1.8.c:
  - Added support for Microsoft Classic Intellimouse 2018 

Features of fw v1.8.b:
  - Added support for Sony PS3 Dualshock3 PAD

Features of fw v1.8.a:
  - Fixed a stupid bug which prevented 16-bit-axis mice to be correctly managed

Features of fw v1.8.9:
 - Changed mousewheel behaviour: 
   - 1. Defaults to no action [hint: probably adding freemouse support in one of next updates]
   - 2. Pressing all three mouse buttons together, board enters "pointer speed setting" mode [Led stops blinking->firmly lit]
   - 3. Rolling Mousewheel now changes pointer speed / DPI sensitivity
   - 4. Pressing all three button together again will save current setting and return to default behaviour [Led starts blinking again]
 - Added support for Logitech MK250
 - Added support for RAPOO 5G Wireless Mouse
 - Added support for ATARI ST Mouse port (ALL devices)
 
Features of fw v1.8.8:
- Added support for Trust IVY 18519 Wireless Mouse
- Added support for Logitech M305 BT Wireless Mouse

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


 
## **DEVELOPMENT**

HID2AMI hardware and firmware were designed, developed and maintained by **Sampedenawa** on behalf of **EmberHeavyIndustries** (an evil worldwide company, whose mission is to rule the world by the mean of reviving Amiga computers), following a discussion born on Italian www.amigapage.it Amiga forum.


## **ASSEMBLY**

 ## **WARNING !!  A COUPLE THINGS YOU MUST UNDERSTAND BEFORE GOING FURTHER**
 
 - **NEVER, NEVER, NEVER connect "both sides" of HID2AMI to a power source at the same time !**
 **This means: do not connect HID2AMI to a PC through the USB port while it is plugged into your Amiga's joy/mouse port !**
 **If you want to upgrade your HID2AMI with bootloader or DFU mode, beware to disconnect it from your Amiga first !**
 
 - **BE AWARE** that when you connect a peripheral to the Amiga's mouse/joy port, the power supply or that peripheral comes from/through that port itself. Amiga control peripheral ports were probably not designed with "mega-rumble-end-of-universe-nuclear-powered" gamepads in mind: while there is generally no risk in connecting "common" mainstream peripherals like the ones have been tested (see above), be aware that improperly connecting an "high" power-demanding device could lead to overheat or even damage the Amiga joy/mouse port. **You can consider the power consumption safety limit roughly around 100mA; exceeding this limit could be dangerous for your Amiga!.** 
 
 ## **You are using HID2AMI at your own risk: I will either not be liable nor responsible for any damage you could cause to your hardware for any use or misuse of HID2AMI together with your systems.**  
 


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

[HID2AMI v2.0.0 SCHEMATICS SHEET](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev2.0.0.sch)

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

[Reference BOM v2.0.0](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev2.0.0_BOM.txt)

[Reference BOM v3.1.0](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev3.1.0_BOM.csv)

### **GERBER FILES**

[HID2AMI v1.0.0 DELUXE GERBER FILES](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist_2019-01-19.zip)

[HID2AMI v1.1.0 DELUXE GERBER FILES](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.redist_2019-02-28.zip)

[HID2AMI v2.0.0 DELUXE GERBER FILES](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev2.0.0_2021-09-24.zip)

[HID2AMI v3.1.0 DELUXE GERBER FILES](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev3.1.0.zip)



### **EAGLE SCHEMATICS AND BOARD LAYOUT**

[HID2AMI v1.0.0 DELUXE SCHEMATICS](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.sch)

[HID2AMI v1.0.0 DELUXE BRD](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.0.0.redist.brd)

[HID2AMI v1.1.0 DELUXE SCHEMATICS](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.redist.sch)

[HID2AMI v1.1.0 DELUXE BRD](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev1.1.0.redist.brd)

[HID2AMI v2.0.0 DELUXE SCHEMATICS](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev2.0.0.sch)

[HID2AMI v2.0.0 DELUXE BRD](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Board/HID2AMI.Deluxe.Rev2.0.0.brd)

### **BOOTLOADER**

Current BOOTLOADER version is 1.4.0. You can freely get it from here [HID2AMIBOOTLOADER](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Firmware/HID2AMIBOOTLOADER.dfu)


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
is distribuited by request, after a minmum donation to support the development, from the author; each instance is strictly tied 1:1 to a particular HID2AMI board. You are not allowed to copy and distribuite HID2AMI APP in any medium or format. 

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
