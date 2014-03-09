Boost-Converter
===============

Description

200-450V variable power supply (with 15V input). The circuit is suitable for powering nixie tubes or charging capacitors.

Instructions

This is a working device, but since there is always room for improvement, it is tagged as "work in progress".

The circuit is basically a "mashup" of a boost converter described on ladyada.net/library/diyboostcalc.html and example circuits described in the 555 datasheet.

The .T3001-file is a Target3001 project file containing schematic and routed two layer PCB layout. 

The Gerber.zip contains all necessary files for PCB production (if you want to order a PCB from a manufacturer)

The output from the boost converter is unregulated, so if you want to use the circuit for anything else than charging a capacitor bank, you should add an electrolytic capacitor in parallel with the output.

Warning: Some capacitors are capable of storing lethal amounts of energy for a very long time (several hours/days). Be very carful if you plan on using this as a charging circuit.

The device can be powered by a 5-15V power supply. 

Component list:
D1: UF4007 diode

D2: 1N4002 diode

R1: 2,2k resistor

R2: 22 k resistor

R3: 1 k trimpot

T1: IRF840 MOSFET

L1: 170 uH inductor

C1 4,7 nF capacitor

C2: 10 nF capacitor

C3: 47 uF electrolytic capacitor

IC2: 555 timer


The design is rather generic. If you want to experiment, you can (In addition to substituting the inductor) replace C1 to modify the frequency range. R1/R2/R3 controls frequency and duty cycle. 

Update (18. May 2012): I have been using this circuit for charging a 450V/6000uF capacitor bank. To minimize the charging time, I removed diode D2. This increases the duty cycle of the 555. In a charger scenario, the initial current will most likely fry D1, and then the mosfet if you don't add a high wattage current limiting resistor on the output( I used a 47 ohm / 5W resistor). It is also a good idea to add a heatsink to the mosfet.
