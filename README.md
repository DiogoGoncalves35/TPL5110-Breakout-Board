# Low Power TPL5110 Breakout Board

![Kicad](https://img.shields.io/badge/KiCad-314CB0.svg?style=for-the-badge&logo=KiCad&logoColor=white)

This small breakout board is designed arround the [TPL5110 Timer](https://www.ti.com/lit/ds/symlink/tpl5110.pdf?ts=1704823351945&ref_url=https%253A%252F%252Fwww.google.com%252F)

<img src="/Images/Board.png">

It's a very simple design, by soldering a THT resistor you can choose the time interval between cicles. 

With 5V power it only draws 50 nA while in standby. Measurements were done with [nrF Power Profiler Kit II](https://www.nordicsemi.com/Products/Development-hardware/Power-Profiler-Kit-2).

<img src="/Images/Consumption.png">

Circuit was tested with IRF9Z24N P-Channel Mosfet. It was added a 10k pull down resistor to the DONE pin for better stability, breadboard parasitic capacitance can cause noise on some lines. The mosfet controls the Arduino Uno board and after 10 seconds the Arduino sends a DONE signal to turn off.

<img src="/Images/Test_Circuit.png">

------------


### Schematic

The [schematic](/PCB/Schematic.pdf) basicly exposes every pin to the connectors. A decoupling capacitor was added on the power rail. The resistor is responsible for the time period.

<img src="/Images/Schematic.png">

------------

### PCB

[This PCB](/PCB) has a very simple design, it's a 1.6 mm board with 2 copper layers, both connect to GND. 

<img src="/Images/PCB.png">


------------

### Known issues

- Parasitic capacitance but it could be related to breadboard


------------

### To-Do

- No updates for now




