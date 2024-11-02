# BSides DFW 2024 Badge Kit Assembly Instructions

# Component List: 

* (QTY 1\) BSides DFW PCB Badge  
* (QTY 1\) 8-pin NESS59 chip (U1)   
* (QTY 3\) 10 KΩ resistors (R1, R3, R4) (Brown/Black/Orange/Gold)  
* (QTY 1\) Battery Holder (BT1)  
* (QTY 1\) Diode (D14)  
* (QTY 1\) 16-pin 74H0595 chip (U2)   
* (QTY 1\) 4.7uF capacitor (C1)  
* (QTY 1\) BC548 NPN transistor (Q1)  
* (QTY 1\) 1 MΩ resistor (R5) (Brown/Black/Green/Gold)  
* (QTY 2\) 1.3 kΩ resistors (R6, R7) (Brown/Orange/Red/Gold)   
* (QTY 1\) SPDT Switch (SW1)   
* (QTY 13\) LED diodes (D1-D13)  
* (QTY 1\) 10 kΩ Potentiometer 

# Assembly Steps: 

**WARNING:**   
**Take care to follow orientation instructions or components may be damaged\!\!\!**  
**Do not insert the batteries until you are absolutely sure the badge is assembled correctly\!\!\!**

Assemble the badge in the following order. This order ensures that you will have plenty of room to solder the component and that other components won’t get in the way. 

## BACK \- Parts should be inserted on the back side and soldered on the front side of the PCB.

1. U1 (NESS59)  \- This is the 8 pin chip.   
   1. ORIENTATION: The ***dot*** on the chip should be on the side closest to the U1 marking and the notch in the footprint. Note the Dot orientation is not the same as U2. 
        
2. R1, R3, & R4 (Brown/Black/Orange/Gold) \- No Orientation  
3. BT1 (Battery Holder)  
   1. ORIENTATION: The \+ on the component should be on the same side as the \+ on the PCB footprint  
4. D14 (Diode)  
   1. ORIENTATION: The band on the component should be on the same side as the band on the PCB footprint  
5. U2 (74H0595) \- This is the 16 pin chip.  
   1. ORIENTATION: The ***notch*** on the chip should be on the side closest to the notch in the footprint. Note the Dot orientation is not the same as U1.
6. C1 (capacitor)  
   1. ORIENTATION: The longer pin on the component should be on the side with the \+ on the PCB footprint.  
   2. NOTE: INCORRECT ORIENTATION WILL RESULT IN DAMAGED COMPONENTS  
7. Q1 (transistor)  
   1. NOTE: The pins may need to be straightened to fit snugly on the PCB.  
   2. ORIENTATION: Match the flat side of the component shape with the flat side on the PCB footprint.  
8. R5 (Brown/Black/Green/Gold) \- No Orientation  
9. R6,R7 (Brown/Orange/Red/Gold) \- No Orientation  
10. SW1 (Switch) \- No Orientation
    1. This may optionally be mounted on the front of the board if desired
    

## FRONT \- Parts should be inserted on the front side and soldered on the back side of the PCB.

11. D1-D13 (diodes)  
    1. ORIENTATION \- Make sure the flat side of the LED matches the same direction as the flat side on the footprint on the back of the PCB. Insert LEDs on the front and solder on the back.   
    2. **NOTE: INCORRECT ORIENTATION MAY RESULT IN DAMAGED COMPONENTS**. Technically, an LED should act as a diode and prevent reverse polarity. However, the reverse voltage protection rating was not checked for this purpose so use caution.
12. Potentiometer (marking missing on the PCB, located next to D13 over an "eye")  
    1. ORIENTATION \- Only fits one way
    2. May be mounted on the back of the board if preferred; this will not affect operation
    3. When testing, Chase speed may be adjusted by turning the small notch inside the potentiometer
