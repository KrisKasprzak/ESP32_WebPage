
<b><h2><center>Sampe code for updating a web page and getting user actions sent back the the microcontroller</center></h1></b>

This sample code will show you how to 1) create an access point, 2) serve a web page, 3) updated just changed data, and 4) get user interactions such as button presses and slider actions sent back to the microcontroller.

You will need an ESP32 and some open source libraries that are delivered with the Arduino IDE such ase WiFi.h, and WebServer.h

<b>WARNING</b>

The ESP32 web libraries have a default max size of a String set to 64K. For small html pages this may be fine, however pages that exceed 64K will fail to load the entire page. Here are a few options in reducing HTML page size
1. remove all indents (granted they make code readable, but each indent is a character)
2. minimize variable name lenghts consider changing ColorForForeground to FColor for example
3. remove blank lines

If your page still exceeds 64K, just increase the buffer size in the library. To see what size you need add a Serial.println(sizeof(XML)) in the; to see what you need.
to increase the page size edit the parameter in:
<br>
C:\Users\Administrator\AppData\Local\Arduino15\packages\esp32\hardware\esp32\3.0.2\cores\esp32\WString.h
<br>
around line 335 change
<br>
//CAPACITY_MAX = 65535
<br>
CAPACITY_MAX =80000 (80K is just and example



<br>
<br>

![header image](https://raw.github.com/KrisKasprzak/ESP32_WebPage/master/screen.jpg)
