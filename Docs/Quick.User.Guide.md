# **HID2AMI QUICK USER GUIDE** 


## **IMPORTANT NOTE READ FIRST**

While playing with HID2AMI and your Amiga, always remember two important things:

- HID2AMI does not have any external power source, so its supply power comes from your Amiga. As a direct consequence, your Amiga will have to supply power to any USB peripheral device cascadely connected to HID2AMI. All of this happens through the Mouse/Joy ports, which therefore must bear the whole supplying current for the ensemble. Whilst there isn't generally any problems at all with typical consumer peripherals, you must avoid connecting high-power-demanding peripherals, without knowledge of what you are doing: in extreme cases you could blow out your Amiga's mouse/joy port current limiting resistors.

- Never connect HID2AMI's USB port to your PC (or any other active device) while it (HID2AMI) is connected to your Amiga's mouse/joy port, no matter if your Amiga is turned off. Simple rule to follow: upgrade flashing HID2AMI must be performed with the board's DB9 (joy) connector unplugged from everyhting.  



## **GETTING STARTED**

Getting started is quite strightforward: 

- connect HID2AMI to your Amiga's mouse or Joypad port (this could be done at any moment, no matters if AMiga is powered on)
- you should notice the "power led" (usually red) firmly lit, and the "running led" (usually green or yellow) blinking roughly twice a second


### **MOUSE OPERATIONS**

- Connect a compatible mouse to the USB port of HID2AMI: the "running led" should slow down to roughly blinking once a second; the mouse has been recognized and initialized
- That's all ! Start playing with you Mouse, and consider customizing you settings as follows


#### **MOUSE CUSTOM SETTINGS**

Default pointer speed recognized by your Amiga depends upon the connected mouse's working parameters, in terms of frequency of position updates and axis bit resolution.
HID2AMI allows you to dynamically adjust the pointer speed, by slowing/fastening within three different degrees.

- To dynamically adjust pointer speed (can be done at any moment): 
 - roll your mousewheel forward to slowdown the pointer travel speed by one step (0% - 25% - 50%)
 - roll your mousewheel backwards to fasten the pointer travel by one step (0% - 25% - 50%)

- To save your speed preference in HID2AMI internal flash, simply push all three buttons (L-R-WHEEL) at the same time: done !


HID2AMI will store and retrieve your settings next time you will connect the mouse. If you have different mice brand/models, HID2AMI automatically saves a dedicated profile for each one, and automatically retrieves it when that particula mouse is connected.

