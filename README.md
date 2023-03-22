## Adafruit CAN Bus FeatherWing - MCP2515 PCB

<a href="http://www.adafruit.com/products/5709"><img src="assets/5709.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit CAN Bus FeatherWing - MCP2515. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/5709

### Description

CAN Bus is a small-scale networking standard, originally designed for cars and, yes, busses, but is now used for many robotics or sensor networks that need better range and addressing than I2C, and don't have the pins or computational ability to talk on Ethernet. CAN is 2 wire differential, which means it's good for long distances and noisy environments.

Messages are sent at about 1Mbps rate - you set the frequency for the bus and then all 'joiners' must match it, and have an address before the packet so that each node can listen in to messages just for it. New nodes can be attached easily because they just need to connect to the two data lines anywhere in the shared net. Each CAN devices sends messages whenever it wants, and thanks to some clever data encoding, can detect if there's a message collision and retransmit later. 

If you'd like to connect your Feather to a CAN Bus, the Adafruit CAN Bus FeatherWing with MCP2515 controller and TJA1051/3 transceiver will work with any and all Feathers! The controller used is the MCP2515, an extremely popular and well-supported chipset that has drivers in Arduino and CircuitPython and only requires an SPI port and two pins for chip-select and IRQ. Use it to send and receive messages in either standard or extended format at up to 1 Mbps.

We've added a few nice extras to this Feather to make it useful in many common CAN scenarios:

* 5V charge-pump voltage generator, so even though you are running 3.3V on a Feather board, it will generate a nice clean 5V as required by the transciever.
* 3.5mm terminal block that can be soldered in to get quick access to the High and Low data lines as well as a ground pin.
* 120 ohm termination resistor on board, you can remove the termination easily by cutting the jumper marked TERM on the top of the board.
* A spot that one can solder an optional (not included!) edge-launch DE-9 connector that is commonly used for connecting to CAN devices. L is connected to pin 2 and H is connected to pin 7. You could then plug this into an ODB-II cable to connect to a car's CAN network - you'll still need software to decode the messages though!
* Pre-connected CS and INT pins on the two pins to the left of the I2C Feather port - usually these are pins #5 and #6 but some feathers may have different numbering! You can cut the bottom solder jumpers and use the breakout pads to connect to any two IO pins you like.

Each order comes with an assembled 'Wing, terminal block and header. You will need to solder in the header yourself but its a quick task.

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
