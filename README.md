# PicoBOB for GRBLHAL

![Logo](/readme_images/logo_sm.jpg)

Expatria Technologies PicoBOB GRBLHAL module

<img src="/readme_images/Pico_Boardpng.png" width="300">

Currently available in our online store:

https://expatria.myshopify.com/products/picobob

Please consider buying a board to support our open-source designs. 

The PicoBOB allows you to use the high performance GRBLHAL motion control system with a traditional Mach3/LinuxCNC parallel-port breakout board.  It is intended to be simple and low cost.  It uses a Raspberry Pi RP2040 MCU and the widely available 5 axis Mach3 breakout board.  The PicoBOB can be easily sourced from JLCPCB.  The complete BOM and fabrications files are in the CAM_OUTPUTS folder for upload.  The design is free to use by all parties, including commercial parties, under the CERN-OHL-S V2 license.  It is our hope that the community finds the design useful and that it may be carried forward to help advance the PrintNC and broader CNC hobby community.

The PicoBOB closely tracks the features of the Mach3 BOB:

1) Up to 5 axes of step/direction control.
3) 10A Spindle relay control.
4) 0-10V analog spindle speed control.
5) 5 general purpose inputs
6) One general purpose output.

The default GRBLHAL builds for the PicoBOB include the following features that are implemented in the RP2040 port of GRBLHAL:

1) Backlash Compensation.
2) Stress-free Autosquaring for the ganged axis
3) Ganged axis offsets to correct for offset homing switches
4) Step rates tested up to 180 KHz on 5 simultaneous axes.

In addition, the board has a USB micro connector for the 5V that is required for the BOB.  There is also a push button to reset the Pi Pico without disconnecting power.

Gerber output files are in the CAM_OUTPUTS folder, along with BOM and Pick and Place files to facilitate easy ordering from JLCPCB.  Now available as a chip-down design in revision B1.  Older A1 revision for Pi Pico module is still hosted in case you want to do the final soldering by hand.  The two designs are functionally identical.

## PicoBOB Overview

<img src="/readme_images/Board_Overview.jpg" width="300">

Usage notes:

Communication with GRBLHAL on the PicoBOB is accomplished via the USBC connection on the PicoBOB (not connected in above images).  A short USB cable is used to provide the required 5V for the BOB.  In addition, the BOB requires an external 12-24V supply.

The Mach3 BOB shares the B axis direction signal with a spindle relay enable signal - only one can be used at a time.  Also on the PicoBOB, the stepper enable signal is modified in the GRBLHAL default map file so that it is used as the coolant output signal.  All of this is configurable by re-building the GRBLHAL firwmare.

<img src="/readme_images/boardpics.png" width="500">
Above shows the PicoBOB A1 with a Pi Pico installed and connected to the Mach3/LinuxCNC parallel BOB.
