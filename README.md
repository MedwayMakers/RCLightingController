# RCLightingController

This is a lighting control unit for a radio controlled boat. It could also be used in any other kind of radio controlled thing such as aircraft, cars, etc.

The Arduino takes a PWM input from a spare channel on an RC radio receiver and uses that as a switch to control different lighting sequences. In this case I have used Channel 5 on the receiver which is read into pin 13 on the Arduinop using the Arduino pulseIn() command to read the PWM timings. There is a 2 state toggle switch on channel 5 on the transmitter which gives output readings of approx 933 and 2093 each time it is toggled. The code detects the state change and jumps to the next sequence on each change of the switch.

The circuit has two transistors, one connected to a 5v regulator and one connected directly to the positive of a 6v or 12v battery. The 5v regulator powers the Arduino and also a 5v spotlight, the second transistor is connected to a load of grain of rice 12v lamps connected in parallel. Pins 16 and 19 (Analog pins A2 and A5 on the Nano) are used to control the transistors.
