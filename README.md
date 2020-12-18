# ps2x_example
PS2X Arduino Library
https://github.com/madsci1016/Arduino-PS2X/zipball/5d2be701af64d826d268301d83119a6d2ad04f15

![Maker Tutor PS2 Joystick](https://1.bp.blogspot.com/-jTm9CcXHktQ/X9xEqPqt5xI/AAAAAAABkdM/mM46gKoHc8kz18BiJuzGuvQzSAsmB6WYwCNcBGAsYHQ/w640-h360/arduino-ps2-joy-pinout.png)
![Maker Tutor Ps2 Joystick](https://1.bp.blogspot.com/-QEuohPLTbG8/X9xGbBvBdBI/AAAAAAABkdc/fE9aWN8I6tMiUEO31lGebDo8zVLk48NOwCNcBGAsYHQ/w640-h360/arduino-ps2-joy-67.png)

1. DATA: This is the data line from Controller to PS2. This is an open collector output and requires a pull-up resistor (1 to 10k, maybe more). (A pull-up resistor is needed because the controller can only connect this line to ground; it can’t actually put voltage on the line).
2. COMMAND: This is the data line from PS2 to Controller.
3. VIBRATION MOTOR POWER
4. GND: Ground
5. VCC: VCC can vary from 5V down to 3V .
6. ATT: ATT is used to get the attention of the controller. This line must be pulled low before each group of bytes is sent / received, and then set high again afterwards. This pin consider as “Chip Select” or “Slave Select” line that is used to address different controllers on the same bus.
7. CLK: 500kH/z, normally high on. The communication appears to be SPI bus.
8. Not Connected
9. ACK: Acknowledge signal from Controller to PS2. This normally high line drops low about 12us after each byte for half a clock cycle, but not after the last bit in a set. This is a open collector output and requires a pull-up resistor (1 to 10k, maybe more).
