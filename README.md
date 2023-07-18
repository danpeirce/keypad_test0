# Testing Adafruit 419 Membrane 3x4 Keypad

We have a class set of the Adafruit 419 membrane 3x4 keypad. This repository provides a simple method to test
the keypads before giving them to students. It is a minor modification to the example **keypad_test** included
in the Adafruit keypad library.

* The Adafruit_Keypad library repository is at https://github.com/adafruit/Adafruit_Keypad 
* The **keypad_test0** repository is simply a modification of the keypad_test example from the Adafruit_Keypad library.

## Using ESP32S2 board for Testing

I'm using the ESP32S2 on a solderless breadboard and the Arduino IDE for testing.

### Modifications to the Code

* using 115200 baud rate which is more typical for the ESP32 board
* simplified code from keypad_config.h and then moved the simplified content directly into **keypad0.ino**
    * with the simplified code there was no need for separate files
    * the example header file had definitions that I thought should be in a ino file. 
      Moving the definitions into the ino file resolves that issue.
* reversed the order of the GPIO pins so that the keybad flex PCB cable would
   not pass over the board when connected and top side of keypad could be 
   kept print side up.

~~~~C 
#define R1    8
#define R2    7
#define R3    6
#define R4    5
#define C1    4
#define C2    3
#define C3    2
~~~~


## Installing Adafruit Keyboard Library

The procedure for installing the library is given here https://learn.adafruit.com/matrix-keypad/arduino 


## The Following is Verbatim from [Adafruit Library](https://github.com/adafruit/Adafruit_Keypad/tree/master)

# Adafruit Keypad Library 

This is a library for using diode multiplexed keypads with GPIO pins on Arduino.

Adafruit invests time and resources providing this open source code, please support Adafruit and open-source hardware by purchasing products from Adafruit!

Written by Dean Miller for Adafruit Industries.
MIT license, all text above must be included in any redistribution