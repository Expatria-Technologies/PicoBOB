# Prebuilt PicoBOB Firmwares

Suggestion is to use the aweseom web builder from IO Engineering.

Breakout Board pin mapping:
http://svn.io-engineering.com:8080/?driver=RP2040&board=PicoBOB

Gecko G540 pin mapping:
http://svn.io-engineering.com:8080/?driver=RP2040&board=PicoBOB_G540

Some older testing firmwares are here to help get things up and running.

grblHAL_PicoBOB_3Axis_xxxx.uf2 is for a basic 3 axis machine.

grblHAL_PicoBOB_Ygang__xxxx.uf2 has a ganged Y axis.  This is used on machines like the PrintNC.

grblHAL_PicoBOB_G540YGANG_221229.uf2 has a ganged Y axis and is updated to support the Gecko G540

Install the firmware by putting the Pi Pico into loading mode and copy them to the USB drive that appears.  The PicoBOB is equipped with a reset button for convenience.  With the Pi pico connected to your PC via USB, hold the white button the the Pico and then pulse the black reset button on the other side of the board. The Pico should appear as a USB drive and you can simply copy the desired firmware.

YGANG pinout is as below:

<img src="/readme_images/BOB_PINOUT_YGANG.png" width="500">
