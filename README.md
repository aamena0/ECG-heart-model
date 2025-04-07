# ECG-heart-model
#Building an Arduino-Based ECG: From Basic Signal to Visual Display

This guide provides a step-by-step approach to creating an ECG (Electrocardiogram) monitoring system using an Arduino. You can start with a simple setup to view the raw ECG signal on the serial plotter and then gradually add complexity by incorporating an OLED display and LED indicators.

#Materials:
Arduino Uno
AD8232 ECG sensor module
Connecting wires
Gel Electrodes
Optional: OLED display (128x64, SSD1306 driver)
Optional: 2 x LEDs (different colors recommended)
Optional: 2 x 220 Ohm Resistors (for LEDs)
Breadboard 
1. AD8232 ECG Sensor Module
A single-lead heart rate monitor front-end designed for ECG and other biopotential measurement applications.

AD8232 Connections (Common to all Steps):
GND: Connect to Arduino GND
OUTPUT: Connect to Arduino Analog Pin A0
LO +: Connect to Arduino Digital Pin A3 (Leads-Off Detection)
LO -: Connect to Arduino Digital Pin A2 (Leads-Off Detection)
SDN: Connect to Arduino Digital Pin 4. You'll usually set this HIGH to enable.
![image](https://github.com/user-attachments/assets/56bc3017-2b8f-4b71-83fc-b9af99ef47ba)

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
