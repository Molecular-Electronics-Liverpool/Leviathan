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

### Tabbed Interface menu Controls  

The tabbed interface menu on the left hand side contains the majority of the controls for choosing & running experiments.  
It consists of 5 tabs:  

* Introduction
* PID Settings
* STM-BJ
* Data Analysis Settings
* Notes

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
* Ramp Height / nm: The retraction length of the STM tip for standard STMBJ measurements (default: 10 nm).  
* Offset / nm: The offset of the midpoint (duty-cycle) of the STMBJ ramps (default: 0 nm).
* Ramp Time / s: The time for each ramp to execute. Together with Ramp Height defines the retraction rate (default: 1 s).
* Sharpening Depth / nm: The ramp height for the periodic tip sharpening, typically much larger than the ramp height to create fresh tip interface (default: 50 nm).
* #Traces/Sharpen: the number of traces that are executed between sharpening ramps (default: 200).
* Sharpening Time / s: The time for each sharpening ramp to execute (default 1 s).
* Ramp Type: defines which type of ramp (Linear or Advanced Ramps) is being run for quick switching between specialised experiments and default STMBJ experiments (default Linear Ramp).
* Ramp Time / s: the actual recorder time for each ramp to cycle.
* Adv BJ Measurement Method: The type of specialised experiment that will be run when 'Advanced Ramps' is chosen in the Ramp type dropdown (default: Piezo hold).

### Data Analysis Settings  

Contains:  
* Maximum Log(G/G0): Controls conductance histogram bin upper range (default: 0.5).  
* Minimum Log(G/G0): Controls conductance histogram bin lower range (default: -6).  
* Maximum Piezo / nm: Controls displacement histogram bin upper range (default: 3.2 nm).  
* Minimum Piezo / nm: Controls displacement histogram bin lower range (default: -0.25 nm).  
* 2DHist intensity: Controls the intensity of the 2D conductance-displacement histogram (default: 100).  
* Upper bound: The upper threshold in Log(G/G0) that must be reached at the beginning of a trace for it to be saved (default: 0.5).  
* Lower bound: The lower threshold in Log(G/G0) that must be reached at the end of a trace for it to be saved (default: -5).  
* Ramps plot: Shows the bias and piezo ramps for the advanced STMBJ methods (default: Blank for regular STMBJ).  


### Notes

This section contains different useful notes for selecting parameters for different advanced STMBJ methods as well as any generally useful information.  


