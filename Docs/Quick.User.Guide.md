# **HID2AMI QUICK USER GUIDE** 


## **IMPORTANT NOTE READ FIRST**

While playing with HID2AMI and your Amiga, always remember two important things:

- HID2AMI does not have any external power source, so its supply power comes from your Amiga. As a direct consequence, your Amiga will have to supply power to any USB peripheral device cascadely connected to HID2AMI. All of this happens through the Mouse/Joy ports, which therefore must bear the whole supplying current for the ensemble. Whilst there isn't generally any problems at all with typical consumer peripherals, you must avoid connecting high-power-demanding peripherals, without knowledge of what you are doing: in extreme cases you could blow out your Amiga's mouse/joy port current limiting resistors.

- Never connect HID2AMI's USB port to your PC (or any other active device) while it (HID2AMI) is connected to your Amiga's mouse/joy port, no matter if your Amiga is turned off. Simple rule to follow: upgrade flashing HID2AMI must be performed with the board's DB9 (joy) connector unplugged from everyhting.  



## **GETTING STARTED**

Getting started is quite strightforward: 

- connect HID2AMI to your Amiga's mouse or joypad port (this could be done at any moment, no matters if Amiga is powered on)
- you should notice the "power led" (usually red) firmly lit, and the "running led" (usually green or yellow) blinking roughly twice a second


### **MOUSE OPERATIONS**

- Connect a compatible mouse to the USB port of HID2AMI: the "running led" should slow down to roughly blinking once a second: the mouse has been recognized and initialized
- That's all ! Start playing with your Mouse, and consider customizing its workign parameters as follows


#### **MOUSE CUSTOM SETTINGS**

Default pointer speed, recognized by your Amiga, depends upon the connected mouse's working parameters, in terms of frequency of position updates and axis bit resolution.
HID2AMI allows you to dynamically adjust the pointer speed, slowing/speeding-up within three different degrees.

- To dynamically adjust pointer speed (it can be done at any moment): 
  - Roll your mousewheel forward to slowdown the pointer travel speed by one step (0% - 25% - 50%)
  - Roll your mousewheel backwards to speedup the pointer travel speed by one step (0% - 25% - 50%)

- **To save your speed preferences** in HID2AMI internal flash, simply **push all three buttons (L-R-WHEEL) together at the same time**: done !


HID2AMI will store and retrieve your settings next time you will connect the mouse. If you have different mice brand/models, HID2AMI automatically saves a dedicated profile for each one, and automatically retrieves it when that particular mouse is connected.


### **GAMEPAD OPERATIONS**

- Connect a compatible joy/gamepad to the USB port of HID2AMI: the "running led" should slow down to roughly blinking once a second: the pad has been recognized and initialized
- You can set your pad to work either in Analog or Digital mode, according to your preferences; start then playing with your pad, and consider customizing its workign parameters as follows
- By default, HID2AMI maps the first six gamepad buttons to the sequence: Amiga1 - Amiga2 - UP - DOWN - Amiga1 - Amiga2. Unfortunately any single different pad declares its buttons in somewhat a random order, so it is not possible for HID2AMI to be sure that the automatic mapping meets your tastes. So, consider customizing your settings as follows


#### **GAMEPAD CUSTOM SETTINGS**

HID2AMI allows the user to freely customize the mapping of any pad's first 4 buttons, more than enough to play any possible Amiga game. Furthermore, HID2AMI automatically saves the gamepad custom mapping into its internal flash, and retrieves it when the pad is connected again. Different brand/models of pads are automatically recognized, and the respective custom profile saves are stored and recalled without any need of user's intervention.

- **To start and perform the mapping procedure**
  - press all together the first 4 buttons of the pad AND pull the left trigger DOWN
  - the running led stops blinking and stands firmly lit: you are in mapping mode
  - press in sequence the buttons you want to map to Amiga1 - Amiga2 - UP - DOWN ; after each acquired mapping, the "runnin led" changes state (lit-unlit-lit-unlit)
  - after mapping the 4th button, your configuration wil be saved, and the "running led" will start blinking again



## **GENERAL TROUBLESHOOTING**

- Device not working or not recognized
  - Speaking in general, HID2AMI has been designed to be mostly able to manage every HID-compliant peripheral devices; unfortunately there is a lot of "partially / not fully / not at all"-hid-compliant-devices out there; some of them deliberately miscompliant (e.g. XboX360, ...), some of them because of poor/cheap/cloned implemenation (even a pad declaring himself being a keyboard has been found and tested ...). If you have one of them and would like having it to painlessly work with HID2AMI, you can try sending a mail to the author, together with your peripheral's HID Report dump.

- Device not responding properly
  - In rare cases, some chinese PS3-clones were found not properly initializing themselves when connected, then responding with wrong direction to analog stick: if the case happens, just unplugging and replugging the pad again should solve the situation
