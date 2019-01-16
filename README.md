# HID2AMI
If you like this project and want to contribute to its further development, please consider donate 1$ or 1EU (paypal friends & family, please).

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/EmberHeavyIndustries)




HID2AMI is an HID mouse to quadrature waveform converter and HID Gamepad adapter for the Amiga (and AtariST also..) series of boards; it allows ANY modern HID mouse (not limited to PS/2-USB) and almost ANY (*) modern digital/analog Gamepad to be connected and enjoyed with our Amiga computers.

(*) At the moment it has been tested with most Logitech Wingman and Thrustmaster series Gamepads. PS3/PC Gamepad support has been added starting from fw 1.5.2. Xbox Gamepad support have to be considered in future releases (Xbox pads does not strictly comply to HID protocol)

There are a few similar free projects out there on the net (the most known is Smallymouse2), as well as a number of "commercial" projects (coccolino, Ryz, ..) but this one has some major advantages:

- it is natively Amiga-oriented;
- it is a lot cheaper;
- hw schematics and pcbs will be (soon) open and free;
- handles and manages any HID mouse, joystick and gamepad with autodiscover of capabilities and automatic button mapping
- it is a 100% Italian project (ok, I admit this one could not be the smartest thing to write on an English board )


-- How does it work ? (in brief):

HID2AMI recognizes and manages any HID device connected to its USB interface; if the device is recognized as an HID mouse, then HID2AMI starts understanding live movements and button pressings of the peripheral, then converting both of them into proper quadrature waveforms (and Amiga mouse button pressings) which can be properly understood by the Amiga itself, as if a quadrature "Amiga" mouse was connected.

If the device is recognized as an HID gamepad, then HID2AMI maps pad's controls on the Amiga Joystick port/interface.
Gamepad's buttons are mapped evenly on Amiga button1/button2 inputs.

There is no need to manually configure the emulation mode: device recognition and operation mode switching are automatically performed by HID2AMI itself.


-- How far is the project complete ?

The final rev. 1.0.0 pcbs are in "production". Two version of HID2AMI exist: Lite version (yellow) and DeLuxe version (blue). They are different in the way outputs to Amiga ports are buffered (DeLuxe version outputs go through mosfet buffers, for maximum compatibility with "weak" amigas ..).


Current firmware 1.4.1 features:

- self configuration of outputs according to board variant (Lite or DeLuxe);
- automatic recognition of any HID mouse;
- automatic recognition of any (*) HID joystick/gamepad;
- support for both digital (hatswitch) and analog x-y gamepad axis;
- automatic emulation mode switch upon peripheral connection (no need of any manual settings);
- self discover and mapping of pad buttons;
- easy firmware upgrade through (windows) PC USB interface;


-- Who developed HID2AMI ?

HID2AMI hardware and firmware were designed and developed by Sampedenawa, following a discussion born on Italian www.amigapage.it Amiga forum.


-- Will it be shared/given away/sold ?

At the moment my idea is to release the schematics as open source, while keeping the firmware code closed: I would like to distribute soon a number of boards to anyone could be interested.
This is why I would like to share this project with other of Amiga fans, but I would not definitively like finding some "wise guy" making money by cloning and selling my project without having spent a minute on helping develop it.


Within 2019/1Q I should be able to manage having a small number of ready assembled boards; I will notify here their availability, should anyone be ineterested in buying a complete one from me, rather than build one on his own from the gerbers. 
