# FLASHING HID2AMI UNDER LINUX

You will need dfu-util from http://dfu-util.sourceforge.net. A recent version (>= 0.8) is recommended, so you will probably need to download and compile it. Versions included in mainstream distributions might not work. This procedure has been tested with the current git version, as of 5 Feb 2019.

## FLASHING THE BOOTLOADER
- Set HID2AMI in DFU-BOOT mode, by selecting position 2-3 for both "BOOT0" and "PA9BOOT" jumpers
- MAKE SURE THAT HID2AMI IS NOT CONNECTED TO YOUR AMIGA MOUSE/JOY PORT
- Connect HID2AMI to any USB port of your PC, by mean of the A-A USB Cable
- Wait 5-10 seconds, then you should see something like the following in your `dmesg`:
```
usb 1-1: new full-speed USB device number 57 using xhci_hcd
usb 1-1: New USB device found, idVendor=0483, idProduct=df11
usb 1-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3
usb 1-1: Product: STM32 0x418 DFU Bootloade
usb 1-1: Manufacturer: STMicroelectronics
usb 1-1: SerialNumber: STM32
```
On my system it takes several seconds and quite a bit of weird errors are reported, but eventually it will settle down to that.
- Run `sudo dfu-util --list`, you should get some output similar to the following:
```
dfu-util 0.9

Copyright 2005-2009 Weston Schmidt, Harald Welte and OpenMoko Inc.
Copyright 2010-2019 Tormod Volden and Stefan Schmidt
This program is Free Software and has ABSOLUTELY NO WARRANTY
Please report bugs to http://sourceforge.net/p/dfu-util/tickets/

Deducing device DFU version from functional descriptor length
Found DFU: [0483:df11] ver=2200, devnum=57, cfg=1, intf=0, path="1-1", alt=1, name="@Option Bytes  /0x1FFFF800/01*016 e", serial="STM32"
Found DFU: [0483:df11] ver=2200, devnum=57, cfg=1, intf=0, path="1-1", alt=0, name="@Internal Flash  /0x08000000/128*002Kg", serial="STM32"
Found Runtime: [05ac:8289] ver=0137, devnum=6, cfg=1, intf=3, path="1-3.3", alt=0, name="UNKNOWN", serial="UNKNOWN"
```
- Focus on the last few lines: these list all devices that support DFU mode connected to the system. Some of them will belong to HID2AMI, but others might refer to other peripherals connected to your computer  (or built into it!). You might want to run the command again with HID2AMI disconnected to see if it finds something in your computer. Two of the lines will refer to HID2AMI, you can identify them as they will be saying `serial="STM32"`. One of those will also say `name="@Internal Flash..."` and this will be the device we need to flash. In order to do so, we need a way to uniquely identify it: in the above case, using the `intf=0` and `alt=0` attributes is enough. Your mileage may vary, be careful as you might damage other devices if you flash them with the wrong firmware. You can also brick your HID2AMI if you change its `Option Bytes`, so please be very careful not to touch them! Let me repeat: **you must take care so that you only work on the `Internal Flash` of your `STM32` device**!
- Download the bootloader from https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Firmware/HID2AMIBOOTLOADER.dfu, change to the directory you saved it to and run: `sudo dfu-util -D HID2AMIBOOTLOADER.dfu -i 0 -a 0`, where `-i` and `-a` are followed by the `intf` and `alt` IDs found above. If you need to pass extra parameters to select the correct device, run `dfu-util --help` to see the full option list and tune the command appropriately. You should get the following output:
```
dfu-util 0.9

Copyright 2005-2009 Weston Schmidt, Harald Welte and OpenMoko Inc.
Copyright 2010-2019 Tormod Volden and Stefan Schmidt
This program is Free Software and has ABSOLUTELY NO WARRANTY
Please report bugs to http://sourceforge.net/p/dfu-util/tickets/

Match vendor ID from file: 0483
Match product ID from file: 0000
Deducing device DFU version from functional descriptor length
Opening DFU capable USB device...
ID 0483:df11
Run-time device DFU version 011a
Claiming USB DFU Interface...
Setting Alternate Setting #0 ...
Determining device status: state = dfuIDLE, status = 0
dfuIDLE, continuing
DFU mode device DFU version 011a
Device returned transfer size 2048
DfuSe interface name: "Internal Flash  "
file contains 1 DFU images
parsing DFU image 1
Target name: HID2AMIBOOT_1.3.0
image for alternate setting 0, (1 elements, total size = 21712)
parsing element 1, address = 0x08000000, size = 21704
Download	[=========================] 100%        21704 bytes
Download done.
done parsing DfuSe file
```
- **NOTE:** If you are not flashing the device for the first time, or if for any reason you get the error message `ERASE_PAGE not correctly executed`, try adding `-s 0:force:unprotect` to the above command line and wait a minute (literally, i.e.: 60 seconds), then retry the original command.

## RETRIEVING YOUR PERSONAL BOARD CODE
If everything went fine, your board can now boot from the BOOTLOADER and is ready to be flashed with the HID2AMI App.

- Set HID2AMI in BOOTLOADER mode, by selecting position 1-2 for "BOOT0" and position 2-3 for "PA9BOOT".
- MAKE SURE THAT HID2AMI IS NOT CONNECTED TO YOUR AMIGA MOUSE/JOY PORT.
- Connect HID2AMI to any USB port of your PC, by mean of the A-A USB Cable: the bootloader should take control, and you should see the activity led on board (LED1) blinking rapidly.
- Run again `sudo dfu-util --list`. The output should not be much different from before, but this time the `ver` field will be different:
```
- Found DFU: [0483:df11] ver=59eb, devnum=88, cfg=1, intf=0, path="1-1", alt=0, name="@Internal Flash   /0x08000000/06*002Ka,122*002Kg", serial="00000000010C"
```
- In order to get a properly signed app, working tied to your board, you have to ask the author for it, by sending him an [email](mailto:EmberHEavyIndustries@gmail.com) together with your personal code, which is what is reported in the `ver` field  (in my case it is `59eb`, yours should obviously be different).

## FLASHING THE HID2AMI APP
The author will send you your personalized app file, in the form "HID2AMIAPP.XXXX.dfu".
- Boot again HID2AMI in BOOTLOADER mode (just as above)
- Run again `sudo dfu-util --list` and check again the IDs of your device. If they have changed, tune the following commands appropriately.
- Run `sudo dfu-util -D HID2AMIAPP-1.7.2-59EB.dfu -i 0`. Note that the `-a` option is no longer necessary, since the `Option Bytes` entry should not appear anymore. Your output should look like the following:
```
dfu-util 0.9

Copyright 2005-2009 Weston Schmidt, Harald Welte and OpenMoko Inc.
Copyright 2010-2019 Tormod Volden and Stefan Schmidt
This program is Free Software and has ABSOLUTELY NO WARRANTY
Please report bugs to http://sourceforge.net/p/dfu-util/tickets/

Match vendor ID from file: 0483
Match product ID from file: 0000
Deducing device DFU version from functional descriptor length
Opening DFU capable USB device...
ID 0483:df11
Run-time device DFU version 011a
Claiming USB DFU Interface...
Setting Alternate Setting #0 ...
Determining device status: state = dfuIDLE, status = 0
dfuIDLE, continuing
DFU mode device DFU version 011a
Device returned transfer size 1024
DfuSe interface name: "Internal Flash   "
file contains 1 DFU images
parsing DFU image 1
Target name: HID2AMI_1.7.2_59EB
image for alternate setting 0, (1 elements, total size = 81928)
parsing element 1, address = 0x0800c000, size = 81920
Download	[=========================] 100%        81920 bytes
Download done.
done parsing DfuSe file
```
- If no errors are reported, you're done! DISCONNECT you HID2AMI board from your PC, put the HID2AMI board in APP mode by by selecting position 1-2 for both "BOOT0" and "PA9BOOT" jumpers, and connect it to any Mouse/Joy port of your Amiga.
- Enjoy!