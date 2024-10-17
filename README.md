# PinPal
PinPal is a handheld device that acts like a controller for your iPhone. It has 4 hardware buttons and a DMD display. It is made specifically for the newly released VPX (Visual Pinball X) app on the Apple iOS app store.

The VPX iOS App has built-in support for a ZeDMD display device, and i've build a specific firmware for the Lilygo T-Display S3 AMOLED device. The display refresh speed is high enough for enjoyable gameplay and there are also different scaling modes available to simulate a DMD pixel display. The ZeDMD firmware has full support for colorized DMD with the help of [Serum](https://github.com/zesinger/libserum).

### Gameplay:

[![VPX Gameplay](https://img.youtube.com/vi/CqxvdAZtwaw/0.jpg)](https://www.youtube.com/watch?v=CqxvdAZtwaw)

### DMD close up: 

[![VPX DMD](https://img.youtube.com/vi/JCEzE09UcEo/0.jpg)](https://www.youtube.com/shorts/JCEzE09UcEo)

There are 4 different scaling methods available; this is using the 2x2 pixel mode ( this is drawn in a 4x4 black pixel block to simulate the DMD effect ).

### Pictures:

<img src="https://github.com/user-attachments/assets/167c5652-8f31-4f30-a548-61e32d66f4b8" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/0e36f419-3ddb-421d-8e22-fe06388dd69a" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/ff31e228-4cdf-416c-bdde-b99032e7bb37" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/4f6e2528-6082-4bd9-8f7d-4d5c7ad7e045" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/faa7a293-437d-4c6f-bf54-5b4bd4f6bc31" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/85e6f304-32de-485e-bb94-c0e83149d9a0" width=50% height=50%>

## Progress
After some weeks of thinkering I have finished the first prototype. This still has some rough edges, but it is fully working as imagined the initial concept. The current version is made for the iPhone Pro Max series; the bigger phones with USB-C connector. I plan to release 4 different versions:
- iPhone 15/16 Pro Max USB-C (already released)
- iPhone 15/16 Pro USB-C
- iPhone 13/14 Pro Max Lighting
- iPhone 13/14 Pro Lighting

Right now i'm not satisfied with the button placement and try some new configs to see what is comfortable. Also i've made a firmware for the ESP32 Zero to emulate a keyboard for the hardware buttons; i plan to convert this firmware to a gamecontroller get rid of the missing onscreen keyboard issue. 

I will release all my 3d printable files in STL and Step form. I encourage others to adapt and change my designs. 

## BOM (Bill of materials)

|Description|Amount|Link|
|---|---|---|
|T-Display S3 AMOLED V2.0 Non-Soldered Pin [H713]| 1x | https://www.lilygo.cc/products/t-display-s3-amoled?variant=43506902368437 |
|ESP32-S3-Zero| 1x | https://www.waveshare.com/esp32-s3-zero.htm |
|Soft dome tactile push buttons|4 buttons (buy a 20 pack) |https://aliexpress.com/item/1005005384244944.html|
|Keycaps with switches (we dont use the switches)|1x|https://aliexpress.com/item/32815260070.html|
|USB-C female 5 pin connector|2x|https://aliexpress.com/item/1005006260700701.html|
|Screws|6x|TBD|
|Screws|6x|TBD|

## Build instructions

Stay tuned, i will document this later.

## Setup instructions

1. Install VPX from the Apple iOS store.
2. Click the cog at the right top to open the VPX Settings.
3. Change the DMD type to "ZeDMD-WiFi".
4. Fill in the IP Adress and use the default port number 3333.
5. Tap Done in the top right, load up a table and have fun!

## Thanks

I would like to thank the following people for help on this project, without them this wouldn't have been possible:

- [Jason Millard (jsm174)](https://github.com/jsm174)
- [Markus Kalkbrenner (mkalkbrenner )](https://github.com/mkalkbrenner)
- [David (zesinger)](https://github.com/zesinger)
