
<b><h2><center>Sampe code for updating a web page and getting user actions sent back the the microcontroller</center></h1></b>

This sample code will show you how to create an access point, serve a web page, updated just changed data, and get user interactions such as button presses and slider actions sent back to the microcontrller.

You will need an ESP32 and some open source libraries.

WARNING

The ESP32 web libraries have a default max size of a String set to 64K. For small html pages this may be fine, however pages > 64K will fail to load the entire page. Here are a few options in reducing HTML page size
1. remove all indents (granted they make code readable, but each indent is a character)
2. minimize variable name lenghts consider changing ColorForForeground to FColor for example
3. remove blank lines

If your page still exceeds 64K, increase the buffer size, to increase the page size edit the parameter in:
<br>
C:\Users\Administrator\AppData\Local\Arduino15\packages\esp32\hardware\esp32\3.0.2\cores\esp32\WString.h
<br>
around line 335 change
<br>
//CAPACITY_MAX = 65535
<br>
CAPACITY_MAX =80000 (80K is just and example, do a Serial.println(sizeof(XML)); to see what you need)



<br>
<br>

![header image](https://raw.github.com/KrisKasprzak/ESP32_WebPage/master/screen.jpg)
