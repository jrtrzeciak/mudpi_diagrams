# Relay
This example shows a relay connected to the Raspberry Pi. The DS2Y-S-DC5V was chosen since it was already included in the [Fritzing](https://fritzing.org/) library. Ensure the relay you choose is suitable for your application. Can the relay handle the voltage and current needed to drive the load? This relay, for example, is rated for 1A at 30VDC.

The coil of this relay is designed for 5V operation. The coil will draw 40mA at 5V. Note, this is too much current for a single Raspberry Pi pin. In order to provide sufficient power to the coil, an N-channel FET is used. When pin 16 of the Raspberry Pi is low, the transistor will be in an off state, and the relay will be de-energized. When pin 16 is high, the transistor will conduct and pull the coil to ground, energizing the relay.

A diode is included to protect against [flyback voltage](https://learn.sparkfun.com/tutorials/diodes/all#diode-applications). 

A terminal block was also included to connect the relay to an offboard load. The NO or NC pins could be used depending on the application.