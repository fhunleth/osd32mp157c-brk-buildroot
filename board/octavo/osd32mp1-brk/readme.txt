Octavo OSD32MP1-BRK

Intro
=====

This configuration supports the Octavo OSD32MP1-BRK development
platform:

  https://octavosystems.com/octavo_products/osd32mp1-brk/

How to build
============

 $ make osd32mp1_brk_defconfig
 $ make

How to write the microSD card
=============================

Once the build process is finished you will have an image called
"sdcard.img" in the output/images/ directory.

Copy the bootable "sdcard.img" onto an microSD card with "dd":

  $ sudo dd if=output/images/sdcard.img of=/dev/sdX

Boot the board
==============

 (1) Insert the microSD card

 (2) Plug a UART cable to the UART pins and run a serial communication
     program.

 (3) Set the boot switches to off, off, on, off to boot off the microSD
     card.

 (3) Plug a USB cable to power-up the board.

 (4) The system will start with the console on UART.
