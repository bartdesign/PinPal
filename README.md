# PinPal
PinPal is a handheld device that acts as a controller for your iPhone. It has four hardware buttons and a DMD display. It is made specifically for the newly released VPX (Visual Pinball X) app on the Apple iOS App Store.

The VPX iOS app has built-in support for a ZeDMD display device, and I've built specific firmware for the Lilygo T-Display S3 AMOLED device. The display refresh speed is high enough for enjoyable gameplay, and there are also different scaling modes available to simulate a DMD pixel display. The ZeDMD firmware has full support for colorized DMD with the help of [Serum](https://github.com/zesinger/libserum).

### Gameplay:

[![VPX Gameplay](https://img.youtube.com/vi/CqxvdAZtwaw/0.jpg)](https://www.youtube.com/watch?v=CqxvdAZtwaw)

### DMD close up: 

[![VPX DMD](https://img.youtube.com/vi/JCEzE09UcEo/0.jpg)](https://www.youtube.com/shorts/JCEzE09UcEo)

There are 4 different scaling methods available; this is using the 2x2 pixel mode ( this is drawn in a 4x4 black pixel block to simulate the DMD effect ).

### Pictures:

<img src="https://github.com/user-attachments/assets/5bec6ebf-a239-4ce7-97a5-c5145f1b9f5f" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/0e36f419-3ddb-421d-8e22-fe06388dd69a" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/ff31e228-4cdf-416c-bdde-b99032e7bb37" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/4f6e2528-6082-4bd9-8f7d-4d5c7ad7e045" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/faa7a293-437d-4c6f-bf54-5b4bd4f6bc31" width=50% height=50%>
<img src="https://github.com/user-attachments/assets/85e6f304-32de-485e-bb94-c0e83149d9a0" width=50% height=50%>

## Progress
-- Update 22-10-2024

- Changed the flipper buttons to the top of the unit; it works a lot better then the old version.
- 2 extra buttons for nudging. I plan to make a sqeeuze to nudge function in combination with the accelerometer in the future and use these buttons for magnasave.
- Added a cable guide system in the bottom plate to easily wire up the unit.
- The dmd display cutout has been changed to a bigger bezel and the mounting solution has been improved and optimized for the lilygo T-display amoled v2.0 solderless.

Todo:
- Better usb-c connector mount, need to lower it a bit and but the connector back a bit.
- In rare cases buttons get a little stuck, need to fiddle some more with tolerances

---

After weeks of tinkering, I've completed the first prototype of my portable pinball handheld device. While it still has some rough edges, it fully works as I originally envisioned. The current version is designed for the iPhone Pro Max series with a USB-C connector. Moving forward, I plan to release four versions:

iPhone 15/16 Pro Max (USB-C) — already released <br>
iPhone 15/16 Pro (USB-C)<br>
iPhone 13/14 Pro Max (Lightning)<br>
iPhone 13/14 Pro (Lightning)<br>

At the moment, I'm experimenting with different button configurations to improve comfort, as I'm not entirely satisfied with the current layout. I’ve also developed firmware for the ESP32 Zero that emulates a keyboard for the hardware buttons. In the next iteration, I’ll be converting this firmware to function as a game controller, which should resolve the issue of the on-screen keyboard interfering with gameplay.

I’ll be releasing all of my 3D printable files in both STL and STEP formats. I’m not a professional 3D modeler; so the models are not perfect :-) <br>
I encourage others to take my designs, improve upon them, and make the project better or start their own versions of this concept!

## BOM (Bill of materials)

|Description|Amount|Link|
|---|---|---|
|T-Display S3 AMOLED V2.0 Non-Soldered Pin [H713]| 1x | https://www.lilygo.cc/products/t-display-s3-amoled?variant=43506902368437 |
|ESP32-S3-Zero| 1x | https://www.waveshare.com/esp32-s3-zero.htm |
|Soft dome tactile push buttons (4PIN) version|4 buttons (buy a 20 pack) |https://aliexpress.com/item/1005005384244944.html|
|USB-C female 5 pin connector|2x|https://aliexpress.com/item/1005006260700701.html|
|Cylinder head screw M4|6x| - I ordered these(the site has all the exact dimensions): https://www.rvspaleis.nl/bouten/binnenzeskant/din-7984/din-7984-[-]-a2-[-]-m4/7984-2-4x12_1 <br> - USA Link of something equivalent: https://belmetric.com/m4x0-7-a2-stainless-din-7984-allen-socket-low-head-cap-screw/?sku=BSH4X12LOWSS |
|Sleeve Nut M4|6x| - I ordered these(the site has all the exact dimensions): https://www.rvspaleis.nl/moeren/hulsmoeren/verzonken-binnenzeskant/9062-2-4_1 <br> - USA link of something equivalent: https://belmetric.com/sleeve-nut-flat-head-stainless/?gad_source=1&gclid=CjwKCAjwjsi4BhB5EiwAFAL0YEJn1d-U1o56CrpPKzjxZ5y5co3S5-NrORw0wPohaRkb9woiMzEqkhoCX0kQAvD_BwE |
|Small copper insulated wires|+- 70 cm| I cut op an old broken USB lead and recycled those wires |

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
