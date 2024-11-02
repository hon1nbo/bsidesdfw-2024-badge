# bsidesdfw-2024-badge
Badge for [BSidesDFW](https://bsidesdfw.com/) and soldering kit for learners! Whilst some experienced hardware folks may think this repo is overkill for a relatively simple badge, the goal is to enable someone to do a fresh start with hardware both in assembly and simple design to try out with KiCAD. Some explanations on choices made are also included to help someone getting started understand why we did things a certain way.

### Contributors
We're all volunteers doing this in spare time; thanks to those that helped out
- ibi5 - concept & artwork
- BearsInPorts - PCB silkscreen art
- hon1nbo - circuit design, PCB Layout

## Assembly
To skip to assembly guidance, we have provided [Instructions](/INSTRUCTIONS.md).

## Basic Operation
The theory of operation for this circuit is very simple, as it's primarily intended for learning and practicing soldering. A 555 timer creates a clock signal, adjustable using a trim resistor, which feeds into the serial and clock inputs of a 74hc595 shift register. This shift register takes the serial signal and outputs a set of parallel signals to the LEDs. However, we're not really using serial data but just shifting the on/off position to the next LED in the sequence. As a note, we're using the 74xxx shift register as a Sink for the LED power so this requires a tri-state compatible variant which is available for most of the 74xxxxx series.

## EDA


### Software
[KiCAD](https://www.kicad.org/) is an open-source EDA tool for PCB and Schematic design. We highly recommend it to anyone getting started with hardware design. We used the SacSym Library Loader for parts to get usable footprints for all components. [Models](/models) are included in this repo since not every KiCAD installation uses this software default, as well as the extra silkscreen artwork located under [Art](/art). General KiCAD files are located in [KiCAD files](/KiCAD%20files), and for fabrication we have included the [Gerbers](/gerbers).
### BOM
Parts were kept simplistic

TKTK BOM

### Design Choices

#### Power
We didn't bother including any voltage regulators. Since we are using a 6v supply in the form of coin cells, and entirely through hole components, a linear regulator would be a bit inefficient and additionally the other form factors at a decent component cost would be hard for a beginner to solder. Thus to keep things simple, we stuck with using the diode's inherent voltage drop.

The LEDs used do not have a significant drop-off in lumens when chasing, and the battery life is just fine for this application based on testing with off-the-shelf 2032 batteries. 

#### Tri-State 74xxxxx logic
We went with a Tri-State 74 series shift register to simplify things. Normally, one would use the output of pins on these set to High to send out a signal. However, by using a tri-state in Sink mode (LEDs power goes to the shift register, then to ground), we were able to have a higher overall current limit across the chip. This allowed us to avoid including drive transisitors for all the LEDs and keep things simpler, and allow us to use brighter LEDs. The downside is the chip cost was ever so slightly higher than a standard 74hc595 variant.

#### Errata
AKA: Screw Ups and weird stuff

- One LED (top left front side) is out of place for the badges issued at BSides due to a shifting error from a trace re-route caused when adjusting a pad size on another component to make an unrelated tab easier to solder. The shift was not caught until after fabrication started, but it has been fixed in the KiCAD files.
- Silkscreen for LEDs is on the back. This saves the headache of multi-colour silkscreen or removing the aesthetic of the front design. We wanted to keep the dots so when unassembled it still keeps the design. The LED orientation is not affected by the silkscreen change.

## Extra Credits
Thanks [SoberDogs](https://soberdogs.weebly.com/) for the use of the sticker art!
