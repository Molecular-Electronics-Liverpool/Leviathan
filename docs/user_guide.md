# Leviathan User Guide

## External Software Dependencies

Leviathan is a software package that handles the real-time control, experimental runs and data acquisition of STMBJ experiments.  
However, it is designed to handle the hardware after the STM approach has been performed by an external software package. This is usually the software that ships with commercial STMs.  
At the University of Liverpool we use a modified Agilent 5500 SPM (for hardware details see 'docs/hardware_guide.md') controlled by PicoView.  
However, any scanning probe microscopy control software capable of disabling its own feedback controller is suitable for use with Leviathan.  

## 1. PicoView Handover

After successfully approaching the STM tip to the surface of substrate in constant current mode, disable the feedback controller on PicoView and enable the 'PID ON?' latch on Leviathan (located on the left hand side).  

> [!TIP]
> If you wish to hand control back over to PicoView, turn the PicoView feedback ON *while* the PID ON? is still active on Leviathan.
> Then, once PicoView feedback is on, disable the feedback on Leviathan by disabling 'PID ON?'
> This ensures a bumpless transfer between PID controllers and avoids crashing the tip into the substrate in an uncontrolled manner - potentially blunting it.

