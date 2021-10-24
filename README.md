# PicoBOB for GRBLHAL

![Logo](/readme_images/logo_sm.jpg)

Expatria Technologies PicoBOB GRBLHAL module

The PicoBOB allows you to use the high performance GRBLHAL motion control system with a traditional Mach3 parallel-port breakout board.  It is intended to be simple and low cost.  It uses a Raspberry Pi Pico RP2040 MCU module and the widely available 5 axis Mach3 breakout board.  The PicoBOB is intended to be easily sourced from JLCPCB.  The complete BOM and fabrications files are in the CAM_OUTPUTS folder for easy upload.  The design is free to use by all parties, including commercial parties, under the CERN-OHL-P V2 license.  It is our hope that the community finds the design useful and that it may be carried forward to help advance the PrintNC and broader CNC hobby community.

The PicoBOB closely tracks the features of the Mach3 BOB:

1) Up to 5 axes of step/direction control.
3) 10A Spindle relay control.
4) 0-10V analog spindle speed control.
5) 5 general purpose inputs
6) One general purpose output.
7) Sparkfun QWIIC differential I2C endpoint - extends the range of I2C and creates a robust data link for real-time jogging and 

In addition, the board has a USB micro connector for the 5V that is required for the BOB.  There is also a push button to reset the Pi Pico without disconnecting power.

## PicoBOB Overview

<img src="/readme_images/Board_Overview.jpg" width="100">

Usage notes:

Communication with GRBLHAL on the PicoBOB is accomplished via the USB connection on the Pi Pico (not connected in above images).  The short USB cable shown above is to provide the required 5V for the BOB.  In addition, the BOB requires an external 12-24V supply.

The Mach3 BOB shares the B axis direction signal with a stepper enable signal - only one can be used at a time.  On the PicoBOB, this is modified in GRBLHAL so that the B axis direction signal is shared with the coolant output signal.

<img src="/readme_images/boardpics.png" width="100">
