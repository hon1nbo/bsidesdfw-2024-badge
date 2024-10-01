# bsidesdfw-2024-badge
Badge for BSidesDFW and soldering kit for learners!

## Basic Operation
The theory of operation for this circuit is very simple, as it's primarily intended for learning and practicing soldering. A 555 timer creates a clock signal, adjustable using a trim resistor, which feeds into the serial and clock of a 74hc595 shift register. This shift register takes the serial signal and outputs a parallel signal. However, we're not really using serial data but just shifting the "on" position to the next LED in the sequence. In this case, we're using the 74xxx shift register as a sink for the LED power so this requires a tri-state compatible variant.

### Contributors
- ibi5 - concept & artwork
- BearsInPorts - PCB layout
- unnamed - PCB layout
- hon1nbo - circuit design

#### EDA Notes
KiCad is used with the SacSym Library Loader for parts. Models will be in /models since not every KiCAD installation uses this by default.

