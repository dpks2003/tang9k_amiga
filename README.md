# tang9k_motorola_amiga

**Video output is adapted for a 5" TFT-LCD module 800x480 Type [SH500Q01Z](https://dl.sipeed.com/Accessories/LCD/500Q01Z-00%20spec.pdf) (Ilitek ILI6122)**

Features
* TFT-LCD Video Output
* Speaker Sound
* PS/2 Keyboard
* Joystick

By default cartridge ROM will be booted (see push button how to suppress).

*Amigo in a FPGA* <br>
![pinmap](\.assets/vic-20-tang.png)<br> <br>

## Tang Push Button utilization
* S1 push button Reset
* S2 Cartridge ROM disable (keep S2 pressed while power-on or excert a S1 push-button Reset, release after)
## Powering
Prototype circuit with Keyboard and Audio Amp can be powered by Tang USB-C connector from PC or a Power Supply Adapter. 

## IP Blocks
For sake of simplification i use block SRAM resources for all memories (SP, SDP, pROM). In addition rPLL, CLK divdiers and GSR resource.


**Pinmap D-SUB 9 Joystick Interface** <br>
![pinmap](\.assets/vic20-Joystick.png)

| Joystick pin | Tang Nano pin | FPGA pin | Joystick Function |
| ----------- | ---   | --------  | ----- |
| 1 | J5 8  | 28   | Joy3 RIGHT |
| 2 | J5 7  | 27 | Joy2 LEFT |
| 3 | J5 6  | 26 | Joy1 DOWN |
| 4 | J5 5 | 25 | Joy0 UP | 
| 5 | n.c. | n.c. | POT Y |
| 6 | J5 9 | 29 | FIRE B.|
| 7 | n.c. | n.c. | 5V |
| 8 | J6 23 | - | GND |
| 9 | n.c. | n.c. | POT X |

**Pinmap PS/2 Interface** <br>
![pinmap](\.assets/ps2conn.png)

| PS/2 pin | Tang Nano pin | FPGA pin | PS2 Function |
| ----------- | ---   | --------  | ----- |
| 1 | J6 10  | 77   | DATA  |
| 2 | n.c.  | - | n.c. |
| 3 | J6 23 | - | GND |
| 4 | J6 18 | - | +5V |
| 5 | J6 11| 76 | CLK |
| 6 | n.c. | - | n.c |
