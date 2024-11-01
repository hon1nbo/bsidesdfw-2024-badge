# bsidesdfw-2024-badge
Badge for BSidesDFW and soldering kit for learners!

## Basic Operation
The theory of operation for this circuit is very simple, as it's primarily intended for learning and practicing soldering. A 555 timer creates a clock signal, adjustable using a trim resistor, which feeds into the serial and clock inputs of a 74hc595 shift register. This shift register takes the serial signal and outputs a set of parallel signals to the LEDs. However, we're not really using serial data but just shifting the on/off position to the next LED in the sequence. As a note, we're using the 74xxx shift register as a Sink for the LED power so this requires a tri-state compatible variant which is available for most of the 74xxxxx series.

#### Assembly & Silkscreen note
The footprint for the LEDs is on the back, despite a front mount. In the KiCAD render it will show the LEDs on the back. This was done to allow the white dots in the silkscreen to remain, which allows for a better design for attendees who do not assemble the badge. The silk screen indicators for the LEDs conflicted with this silkscreen and, barring multi-colour UV PCB printing, would make for an unusable silkscreen. So the decision was made to place the LED silkscreen on the back for assembly purposes. The orientation is correct for putting LEDs on the front, so you can place the flat size/anode pin in the expected location based on the silkscreen from either side of the board.

### Contributors
We're all volunteers doing this in spare time; thanks to those that helped out
- ibi5 - concept & artwork
- BearsInPorts - PCB silkscreen art
- hon1nbo - circuit design, PCB Layout

#### EDA Notes
KiCad is used with the SacSym Library Loader for parts. Models will be in /models since not every KiCAD installation uses this by default.

#### Errata
- One LED (top left) is out of place for the badges issued at BSides due to a shifting error from a trace re-route caused when adjusting a pad size on another component to make an unrelated tab easier to solder. The shift was not caught until after fabrication started, but it has been fixed in the KiCAD files.


### Extra Credits
Thanks [SoberDogs](https://soberdogs.weebly.com/) for the use of the sticker art!