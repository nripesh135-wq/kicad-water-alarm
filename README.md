# Water Leak Alarm

A simple water leak detector board designed in KiCad 9.0. It uses an N-channel MOSFET to trigger an active buzzer when water bridges the sensor contacts.

## How it works
The circuit relies on a basic voltage divider. The gate of the 2N7000 MOSFET is tied to ground through a massive 10MΩ pull-down resistor. This keeps the gate at 0V so the buzzer stays off, and it prevents false alarms from ambient static in the air.

When a drop of water (which naturally conducts a little bit of electricity) touches the two sensor wires, it creates a bridge between the 9V power supply and the MOSFET gate. Because the water's resistance is much lower than 10MΩ, the 9V side pulls the gate voltage high. This turns on the MOSFET, completes the circuit to ground, and sounds the buzzer.

## Project Images

### Schematic
![Schematic](schematic.png)

### Board Layout
![PCB Layout](pcb-layout.png)

### 3D Render
![3D Render](3d-render.png)

## Parts List
* Q1: 2N7000 (N-Channel MOSFET)
* R1: 10MΩ Resistor (Pull-down)
* R2: 6.8KΩ Resistor
* C1: 1nF Capacitor (Noise filtering)
* BZ1: Active Buzzer
* D1: Standard 5mm LED
* Hardware: Screw terminal (J2) and DC Barrel Jack (J1)
