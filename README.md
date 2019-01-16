# HID2AMI
If you like this project and want to contribute to its further development, please consider donate 1$ or 1EU (paypal friends & family, please).

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/EmberHeavyIndustries)




**HID2AMI** is an **HID mouse to quadrature waveform converter** and **HID Gamepad adapter** for the Amiga (and AtariST also..) series of boards; it allows ANY modern HID mouse (not limited to PS/2-USB) and almost ANY (*) modern digital/analog Gamepad to be connected and enjoyed with our Amiga computers.

(*) At the moment it has been tested with most Logitech Wingman, Thrustmaster series Gamepads and PS3/PC Gamepad clones. Xbox Gamepad support have to be considered in future releases (Xbox pads does not strictly comply to HID protocol). Working for any and every existing Gamepad cannot be guaranteed, but if you find a Pad which does not work with HID2AMI, you are encouraged to contact the author and supply him its "HID Report Descriptor" to be investigated.


**HOW DOES IT WORK** (in brief):

HID2AMI recognizes and manages any HID device connected to its USB interface; if the device is recognized as an HID mouse, then HID2AMI starts understanding live movements and button pressings of the peripheral, then converting both of them into proper quadrature waveforms (and Amiga mouse button pressings) which can be properly understood by the Amiga itself, as if a quadrature "Amiga" mouse was connected.

If the device is recognized as an HID gamepad, then HID2AMI maps pad's controls on the Amiga Joystick port/interface.
Gamepad's buttons are mapped evenly on Amiga button1/button2 inputs.

There is no need to manually configure the emulation mode: device recognition and operation mode switching are automatically performed by HID2AMI itself.


**PROJECT STATUS**

  **HW AND SCHEMATICS
  
  **HID2AMI LITE    hw v1.0.0
  
  **HID2AMI DeLuxe  hw v1.0.0
  
  *(Two version of HID2AMI exist: Lite version (yellow) and DeLuxe version (blue). They are different in the way outputs to Amiga ports are buffered (DeLuxe version outputs go through mosfet buffers, for maximum compatibility with "weak" amigas).*

  **FIRMWARE
  
   **HID2AMI BOOTLOADER fw v1.2.0
   **HID2AMI APP        fw v1.5.2

   Features of fw v1.5.2: 
    - Unified firmware, self configuring according to board variant (Lite or DeLuxe);
    - Automatic recognition of any HID mouse;
    - Automatic recognition of any (!) HID joystick/gamepad;
    - Full support for both USB 1.1 and USB 2.0 periperhals;
    - Support for both digital (hatswitch) and analog x-y gamepad axis;
    - Automatic emulation mode switch upon peripheral connection (no need of any manual settings);
    - Self discover and mapping of pad buttons (limited to first 6);
    - Easy firmware upgrade through (windows) PC USB interface;


**DEVELOPMENT

HID2AMI hardware and firmware were designed, developed and maintained by **Sampedenawa** on behalf os **EmberHEavyIndustries** (an evil worldwide company, whose mission is to rule the world by the mean of reviving Amiga computers), following a discussion born on Italian www.amigapage.it Amiga forum.


**ASSEMBLY

**Schematics and pcb gerbers** of HID2AMI are open source, released under the Creative Commons CC BY-NC license.
This means that you are free to:

  **Share** — copy and redistribute the material in any medium or format
    
  **Adapt** — remix, transform, and build upon the material 
    
Under the following terms:

   **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
    
   **NonCommercial** — You may not use the material for commercial purposes.
    
   **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
    
   **No additional restrictions** — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.
   


**HID2AMI BOOTLOADER** is free to download, copy and redistribuite.

**HID2AMI APP** is distribuited by request to the author, and each instance is strictly tied 1:1 to a particular HID2AMI board.

This is why I would like to share this project with other of Amiga fans, but I would not definitively like finding some "wise guy" making money by cloning and selling my project without having spent a minute on helping develop it.


Within 2019/1Q I should be able to manage having a small number of ready assembled boards; I will notify here their availability, should anyone be ineterested in buying a complete one from me, rather than build one on his own from the gerbers. 

**LICENSE

**WARRANTY AND IMPORTANT NOTES

