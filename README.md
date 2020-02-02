This is an archive of the code, binaries and schematics for the 3DP-Vert project, also known as the sw3dprousb or sw3dpro project, that was once hosted at http://code.google.com/p/sw3dprousb written by Detlef "Grendel" Mueller (detlef@gmail.com). More information on the project and code is available in the [3DPro.c file header](https://github.com/codebling/sw3dprousb/blob/master/src/3DPro.c). 

The [adapt-ffb-joy project](https://github.com/tloimu/adapt-ffb-joy) includes some of the 3DP-Vert code but is aimed specifically at enabling force feedback in the Force Feedback Pro joystick. 

The [FFB-Vert Project](http://www.iowajohnsons.com/FFBVert/FFBVert.html) (you may need to visit the home page http://www.iowajohnsons.com prior to visiting the FFBVert page in order to view it, or you may see an online pharmaceuticals site) is a hardware project which hosts a design for a printed circuit board. The circuit board allows all of the needed components to be mounted. There are no software alterations, and the hardware plans are the same (except that pin 13 is tied to pin 11). FFB-Vert sold assembled adapters (with cases), but seems to have stopped assembling and selling adapters in late 2015. 


# MS OverDrive protocol to USB HID adapter

sw3dprousb (aka 3DP-Vert) is a device to connect a Microsoft SideWinder 3D Pro, 3D Pro Plus, Precision Pro, or Force Feedback Pro joystick as a generic USB HID joystick to a computer while retaining full functionallity (8-way hat, slider, and all buttons) at a high readout rate (333Hz) with low latency (< 2ms).

The current version bases on a Teensy 2.0 development board and is very easy to copy.

## Original instructions

Taken from this post: http://www.descentbb.net/viewtopic.php?p=250537#250537

Here is the most-easy-to-copy-yet version of the 3DP-Vert, it's even almost kid & pet safe ;)

What you will need:

1 Teensy 2.0 board - http://www.pjrc.com/store/teensy_pins.html $21 (PJRC)
1 PBC15F - http://www.winford.com/products/pbc15.php $8 (Winford)
1 Breadboard - http://www.radioshack.com/product/index.jsp?productId=2734155 $8.99 (RadioShack)
1 Wire kit - http://www.radioshack.com/product/index.jsp?productId=2103801 $5.99 (RadioShack)
2 2.2kOhm resistors - http://www.radioshack.com/product/index.jsp?productId=2994580 $.99 (5) (RadioShack)
2 .001uF capacitors - http://www.radioshack.com/product/index.jsp?productId=2062362].001uF capacitors $1.49 (RadioShack)

You will need to load the [hex file from the `dist` directory](https://raw.githubusercontent.com/codebling/sw3dprousb/master/dist/3DPro32u4-10.hex) onto your Teensy using the [Teensy loader application](http://www.pjrc.com/teensy/loader.html). 

Use the pictures below show how to assemble the adapter on a broadboard. Note the wires in the upper left corner (circled in the pic). Make sure it looks the same to prevent the pins from the PBC15F adapter digging into the wires. Also note the corner of the PBC15F adapter close to the Teensy board, I ground it
down a bit using some sandpaper.

Once you built the 3DP-Vert, connect it to your PC with an USB A-miniB cable, push the button on the board
and use the Teensy loader to program the [hex file](https://raw.githubusercontent.com/codebling/sw3dprousb/master/dist/3DPro32u4-10.hex). That's it. :)

Here are pictures of breadboard setup on the Teensy 2.0
![Breadboard by itself](https://raw.githubusercontent.com/codebling/sw3dprousb/master/r3BB2schem.jpg)
![1st view of broadboard with Teensy 2.0 and port mounted](https://raw.githubusercontent.com/codebling/sw3dprousb/master/r3BB2view1.jpg)
![2nd view of broadboard with Teensy 2.0 and port mounted](https://raw.githubusercontent.com/codebling/sw3dprousb/master/r3BB2view2.jpg)


Here is a picture of the circuit with a Teensy++. The pinouts of the Teensy++ are different from the Teensy 2.0 and above, so only use this picture if appropriate. 
![View of broadboard with Teensy++ and port mounted](https://raw.githubusercontent.com/codebling/sw3dprousb/master/r3BBT%2B%2B.JPG)
