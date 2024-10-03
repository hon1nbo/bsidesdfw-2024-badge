# bsidesdfw-2024-badge
Badge for BSidesDFW and soldering kit for learners!

## Basic Operation
The theory of operation for this circuit is very simple, as it's primarily intended for learning and practicing soldering. A 555 timer creates a clock signal, adjustable using a trim resistor, which feeds into the serial and clock of a 74hc595 shift register. This shift register takes the serial signal and outputs a parallel signal. However, we're not really using serial data but just shifting the "on" position to the next LED in the sequence. In this case, we're using the 74xxx shift register as a sink for the LED power so this requires a tri-state compatible variant.

#### Assembly & Silkscreen note
The footprint for the LEDs is on the back, despite a front mount. In the KiCAD render it will show the LEDs on the back. This was done to allow the white dots in the silkscreen to remain, which allows for a better design for attendees who do not assemble the badge. The silk screen indicators for the LEDs conflicted with this silkscreen and, barring multi-colour UV PCB printing, would make for an unusable silkscreen. So the decision was made to place the LED silkscreen on the back for assembly purposes.

### Contributors
- ibi5 - concept & artwork
- BearsInPorts - PCB layout
- unnamed - PCB layout
- hon1nbo - circuit design

#### EDA Notes
KiCad is used with the SacSym Library Loader for parts. Models will be in /models since not every KiCAD installation uses this by default.

