---
title: AC Box Assembly instructions
author: Sasha Zibrov
date: '2019-08-22'
categories:
  - instructions
  - hardware
---
## Assembly instructions

### 1. Prepare the AD9854 Board

The original evaluation board from analog devices is no longer sold, instead we buy boards from amazon or ebay, that could be found by searching for ad9854. The boards look like this:
<br>
<img align="middle" width="400px" alt="Board" src="img/acbox_board.jpg">

to use this board you first need to make sure that **pin 70** "S/P Select" is set to serial programming mode (**LOW**),
<br>
<img align="middle" width="400px" alt="Board pinout" src="img/acbox_pinout.png">

<br>
To do this, take off the heatsink and expose the AD9854 chip (left), using a razor blade break the pin (right)
<p float="center">
	<img width="400px" alt="chip overview" src="img/acbox1.png">
	<img width="400px" alt="chip zoomin" src="img/acbox2.png">
</p>

Set the Timer **W1 Jumper** into the left most position:
<br>
<img align="middle" width="400px" alt="Board" src="img/acbox3_jumper.jpg">
<br>
Finally, reapply thermal paste to the chip and reinstall the heatsink.

### 2. Solder the Arduino Shield
**OSHParK** [board link](https://oshpark.com/shared_projects/UQsKJloo)


Now solder headers, screw terminals, Jack Receptacle, resistors, capacitors, the voltage regulator, the flip flop, the xtal to the DCBOX Arduino shield (see below). You can ensure a good fit to the Arduino if you solder the headers with the shield in place, just make sure not to overheat the Arduino (be quick and minimize soldering iron heat).

<p float="center">
	<img width="400px" alt="Unpopulated Shield" src="img/shield_empty.jpg">
	<img width="400px" alt="Populated Shield" src="img/shield_final.png">
</p>

### Assembled ACBox
<img width="600px" alt="chip zoomin" src="img/acbox_assembled.png">
