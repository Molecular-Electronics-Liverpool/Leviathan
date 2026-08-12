# Leviathan User Guide

## External Software Dependencies

Leviathan is a software package that handles the real-time control, experimental runs and data acquisition of STMBJ experiments.  
However, it is designed to handle the hardware after the STM approach has been performed by an external software package. This is usually the software that ships with commercial STMs.  
At the University of Liverpool we use a modified Agilent 5500 SPM (for hardware details see 'docs/hardware_guide.md') controlled by PicoView.  
However, any scanning probe microscopy control software capable of disabling its own feedback controller is suitable for use with Leviathan.  

## PicoView Handover

After successfully approaching the STM tip to the surface of substrate in constant current mode, disable the feedback controller on PicoView and enable the 'PID ON?' latch on Leviathan (located on the left hand side).  

> [!TIP]
> If you wish to hand control back over to PicoView, turn the PicoView feedback ON *while* the 'PID ON?' is still active on Leviathan.
> Then, once PicoView feedback is on, disable the feedback on Leviathan by disabling 'PID ON?'.
> This ensures a bumpless transfer between PID controllers and avoids crashing the tip into the substrate in an uncontrolled manner - potentially blunting it.

## Front Panel Controls

The tabbed interface menu on the left hand side contains the majority of the controls for choosing & running experiments.  
It consists of 5 tabs:  

### Introduction

Contains general information on keyboard shortcuts, filename formatting requirements, methods of controlling the offset manually (in the colloquially named 'James' mode) and some general notes containing known bugs etc...

### PID Settings

Contains:  
* PID Gains (default: proportional gain = -0.0100, integral time = 0.0001 min, derivative time = 0.0000 min).
* Setpoint for the PID controller (default: 0.1 V from transimpedance amplifier output).
* PID Runtime in seconds.

### STM-BJ

Contains:  
* Ramp On/Off: Turns the experiment ramp on or off (default: off).

### Data Analysis Settings


### Notes


