
# **HID2AMI HOW TO SUBMIT AN HID DUMP** 


## **PREREQUISITES**

In order to submit an useful dump to the author, a minimal setup comprise:

 - A windows OS machine
 - Free USB Tree View tool [USBTREEVIEW](https://www.uwe-sieber.de/usbtreeview_e.html#download)
 - For advanced analysis: USBLyzer software (free trial can be d/loaded form [HERE](http://www.usblyzer.com/download.htm)

## **INSTRUCTIONS for USBTREEVIEW**

 - 1) Plug the peripheral device you want the HID information dumped in a free USB socket on your MS Windows PC
 - 2) Launch UsbTreeView
 - 3) In the left pane, highlight select the device you want to dump (e.g Logitech USB Wheel Mouse in the example pic below)
 - 4) Wait until the right pane is populated (fraction of seconds)
 - 5) Press Right Mouse Button (of your PC's mouse) and select "Copy Report From Here"
 - 6) Paste the result within a text file, name it (the file) something like "xxxx.Mouse.HID.dump.txt"
 - 7) Send the file to the author
 
 
 ![HID2AMI](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Pics/DumpHID.jpg)


## **INSTRUCTIONS for USBLYZER**

 - 0) Download and install USBLyzer free trial version
 - 1) Plug the peripheral device you want the HID information dumped in a free USB socket on your MS Windows PC
 - 2) Launch USBlyzer
 - 3) In the left pane, highlight select the device you want to dump 
 - 4) Look at the "USB Properties" pane, and save its whole content to text file for submission (Figure 1 below)
 - 5) Start a capturing session:  press "Start Capture" button on the toolbar and USB analyzer software starts monitoring USB traffic going through the selected device. Leave it running for a few seconds, while interacting with your peripheral (e.g. press the buttons, move stick, move mouse - if possible do one thing at a time -)
 - 6) Stop capturing session, save the recorded data (in a file with *.ulz extension) 
 - 7) Send both the files to the author
 
 Figure 1)
 ![FIGURE1](http://www.usblyzer.com/img/tour/usb-properties-panel-bg.png)
 
 Sample USB Properties dump file in text format
![USBPROP](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Microsoft%20IntelliMouse.%20Optical%20-%20HID.txt)

Sample Capture "Ulz" file
![ULZFILE](https://github.com/EmberHeavyIndustries/HID2AMI/blob/master/Docs/Microsoft%20IntelliMouse.%20Optical.ulz)

 
