# MS OverDrive protocol to USB HID adapter

sw3dprousb (aka 3DP-Vert) is a device to connect a Microsoft SideWinder 3D Pro, 3D Pro Plus, Precision Pro, or Force Feedback Pro joystick as a generic USB HID joystick to a computer while retaining full functionallity (8-way hat, slider, and all buttons) at a high readout rate (333Hz) with low latency (< 2ms).

The current version bases on a Teensy 2.0 development board and is very easy to copy.

## Original instructions

Hosted on http://code.google.com/p/sw3dprousb

Taken from this post: http://www.descentbb.net/viewtopic.php?p=250537#250537

Here is the most-easy-to-copy-yet version of the 3DP-Vert, it's even almost kid & pet save ;)

What you will need:

1 Teensy 2.0 board - http://www.pjrc.com/store/teensy_pins.html $21 (PJRC)
1 PBC15F - http://www.winford.com/products/pbc15.php $8 (Winford)
1 Breadboard - http://www.radioshack.com/product/index.jsp?productId=2734155 $8.99 (RadioShack)
1 Wire kit - http://www.radioshack.com/product/index.jsp?productId=2103801 $5.99 (RadioShack)
2 2.2kOhm resistors - http://www.radioshack.com/product/index.jsp?productId=2994580 $.99 (5) (RadioShack)
2 .001uF capacitors - http://www.radioshack.com/product/index.jsp?productId=2062362].001uF capacitors $1.49 (RadioShack)

The program image (from Google code) and the Teensy loader application - http://www.pjrc.com/teensy/loader.html

Use the pictures found on the Google code page as a guide to build that thing, note the wires in the upper
left corner (circled in the pic). Make sure it looks the same to prevent the pins from the PBC15F adapter
digging into the wires. Also note the corner of the PBC15F adapter close to the Teensy board, I ground it
down a bit using some sandpaper.

Once you built the 3DP-Vert, connect it to your PC with an USB A-miniB cable, push the button on the board
and use the Teensy loader to program the 3DPro.hex image. That's it. :)
