# CEM3396 
*Figuring out how to make use of surplus CEM3396 chips*
![cem 3396 chip](https://github.com/ekosynth/CEM3396/blob/master/images/cem3396_chip.JPG)
## Overview
* [Introduction to CEM3396](#introduction-to-cem3396)
* [Synths that use the CEM3396](#synths-that-use-the-cem3396)
* [Making a testbed for the CEM3396](#making-a-testbed-for-the-cem3396)

## Introduction to CEM3396
The CEM3396 is a microprocessor controlled dual waveshaper with an integral VCF and VCA. It was manufactured in 1984 by Curtis Electromusic Specialities. As far as Google knows, it was only use in the following three synths:

## Synths that use the CEM3396
- Cheetah MS6
- Oberheim Matrix-6 & Matrix 6-R
- Oberheim Matrix-1000 (narrow version)

## Making a testbed for the CEM3396
![cem 3396 circuit](https://github.com/ekosynth/CEM3396/blob/master/images/basic_connections.PNG)

### Power
The datasheet recommends an unconventoial ideal power supply of +12V positive and -5V negative. However, it mentions the chip can tolerate a maximum of 25V across the rails. Thus for the purposes of experimenting +/-12V is usable.

There are 11 control voltage inputs and they require 0-5V input. Thus a 5V supply will also be required. This could be most easily achieved using a 7805 regulator on the +12V supply.

### Oscillator
The CEM3396 contains waveshaping circuitry, but not oscillating circuitry. Thus an external source of oscillation and frequency control is required. 

The Oberheim Matrix-1000 used a crystal oscillator that oscillates at (how many?)MHz which is divided down to the required frequency by an 82C54 programmable interval timer.
