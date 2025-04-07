# ECG-heart-model
#Materials: 
#Arduino ECG with OLED Display and LED Indicators
This project demonstrates how to build a simple ECG (Electrocardiogram) display using an Arduino, an AD8232 ECG sensor module, an OLED screen, and LED indicators. The OLED screen visualizes the heart's electrical activity in real time, while the LEDs blink in response to the P-wave and QRS complex of the ECG signal.
Materials:
Arduino Uno
AD8232 ECG sensor module
OLED display (128x64, SSD1306 driver)
2 x LEDs (different colors recommended)
2 x 220 Ohm Resistors (for LEDs) (optional)
Connecting wires
Breadboard
Gel Electrodes
#1. AD8232 Module
The AD8232 is a single-lead heart rate monitor front-end designed for ECG and other biopotential measurement applications. It's an integrated module that simplifies the process of acquiring and conditioning ECG signals.

AD8232 Connections:
GND: Connect to Arduino GND
OUTPUT: Connect to Arduino Analog Pin A0
LO +: Connect to Arduino Digital Pin A3 (Leads-Off Detection)
LO -: Connect to Arduino Digital Pin A2 (Leads-Off Detection)
SDN: Connect to Arduino Digital Pin 4 and set to HIGH to enable
2. OLED Display

We'll use a small OLED display to visualize the ECG waveform.

OLED Connections:

GND: Ground
VCC: Power (3.3V or 5V, check your OLED's specifications)
D0 (CLK, SCK): Clock signal - Connect to Arduino Digital Pin 13
D1 (MOSI, SDA): Data signal - Connect to Arduino Digital Pin 11
RES (Reset): Resets OLED - Connect to Arduino Digital Pin 9
DC (Data/Command): Tells if data is a command - Connect to Arduino Digital Pin 8
CS (Chip Select): Selects the OLED - Connect to Arduino Digital Pin 10
3. LED Connections

We will use two LEDs to indicate the P-wave (SA node activity) and the QRS complex (AV node activity).

LED 1 (P-wave indicator):
Anode (longer leg) of the LED connects to Digital Pin 11 (through a 220-ohm resistor).
Cathode (shorter leg) of the LED connects to Arduino GND.
LED 2 (QRS complex indicator):
Anode (longer leg) of the LED connects to Digital Pin 9 (through a 220-ohm resistor).
Cathode (shorter leg) of the LED connects to Arduino GND.
4. Breadboard Diagram
(insert photo)
