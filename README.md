# EurorackPowerRailRev2

Eurorack power rails connect have the purpose of connecting the power supply in the case to your modules. This power board is a simple but feature-rich design to power your eurorack modules.

![overview_photo](https://github.com/drChungus/EurorackPowerRailRev2/blob/d43d31ea04be847787aec6884cd60757d68648a9/img/IMG_20250401_181807.jpg)

This design has 8 connectors every 100mm, which makes it relative space efficient among power buses. Also, using jumpers, boards next to each other can be connected, which practically makes this power bus mudular. If you are building your case with weird shapes and sizes, look no further for power distribution.

The parts being used are easy to obtain and the board can be populated in no time with minimal soldering experience. While the building process can be considered easy you should be mindful about the quality of the soldered connections. As an example, see [this guide](https://learn.adafruit.com/adafruit-guide-excellent-soldering/common-problems) for an overview of how your soldering should look like.

## Featuress

- 8pcs of power connectors, 10 pin or 16 pin, shrouded or simple male headers
- 6 holes for mounting
- Multiple boards can be interconnected using jumpers in the corners
- Screw terminal connectors on every corner
- [Optional] On-board 5V line converter with protection diodes and buffer capacitors for LM7805 style regulators.


## Parts

Use ~100nF for the ceramic and ~47uF for the electrolitic caps. The caps for the converter are 1nF tantalum. Use caps with at least 25V tolerance and keep in mind that electrolitic and tantalum capacitors have a correct orientation.

The resistors for the LEDs are up to your taste but a value between 1k and 10k should work fine.

I recommend using 1N4004 for the diodes.

For illustration, here is the unpopulated PCB with all the parts.

## Assembly

For the assembly, in addition to the parts you will need a soldering iron, solder, tweezers and any related tools according to your preference.

You should start with the pin headers, as they are the most sensitive for allignment. Take your time and solder all headers while positioning them perpendicular to the PCB. If you are using 16-pin connectors, this will give you 128 solder joints. Start with soldering one pin and use this single joint to position the pins. You may also plug a ribbon cable to make sure all pins are well alligned.

Once the main headers are dealt with add the 3-pin headers to the corners. Jumpers can be used to connect neighbouring boards using these headers.

Capacitors should come next, ceramic ones can go in either way, but electrolitic capacitors must be oriented correctly. The minus sign on the board marks the negative lead for the caps.

You can add LEDs and their current limiting resistors as well, thes will indicate power on all three power lines.

The board can be fitted with an LM7805-style power converter to get the 5V bus from the 12V line. This will requrie two additional capacitors (tantalum according to the reference design) and diodes two reverse voltage protection. The 7805 regulator can be laid flat on the PCB, but if higher currents are pulled on the 5V line you may want to add a heatsink instead. Discrete replacements also exist for the 7805, but these keep in mind that these are use switching to convert voltage which may make your system a bit more noisy. 

Wires can be used to connect the power supply to the bus board via screw terminals. These should be the last components you add as they are the tallest.

With this the build should be complete, rinse and repeat for the rest of the boards.



(CC BY-SA 4.0)
