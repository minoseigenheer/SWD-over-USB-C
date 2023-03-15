# SWD over USB-C
 Use SWD (single wire debugging) over USB-C with debug accessory mode.
 https://en.wikipedia.org/wiki/USB-C#Debug_Accessory_Mode

 If CC1 and CC2 are both pulled high the target device needs to detect the debug mode and enable the SWD lines.
 The target device schematics shows how the detection is done.


 ## USB-C pinout
 Because 5 additional debug pins where enough for me I decided for a reversable pin configuration and kept the USB 2.0 differential pair connected in the debug mode.
```
 A normal USB-C cable can not be used because they don't pass trough CC1 and CC2.
```
 <img src="images/SWD over USB-C Pinout-01.png" width="600" alt="SWD over USB-C pinout"/>
 
 ## Debugger connections
 ### ST-Link V2 clones [IDC10]
 Available for a few dollars from china.
 https://nl.aliexpress.com/w/wholesale-ST%2525252dlink-V2.html
 The clones don't bring out SWO (printf traces) but you can modify it yourself. https://sudonull.com/post/20076-Completion-of-the-Chinese-ST-Link-v2-add-the-SWO-debug-information-output-interface-and-foot-reset
 ### ST-Link V3 mini [STDC14]
 https://www.st.com/en/development-tools/stlink-v3minie.html
 or the older https://www.st.com/en/development-tools/stlink-v3mini.html

 ## USB-C to SWD connector board
<img src="images/SWD over USB-C top render.png" width="600" alt="SWD over USB-C connector"/>