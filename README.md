# 8086-dc-motor-speed-control
# 8086-Based DC Motor Speed Control Using PWM

A microprocessor and interfacing project for real-time DC motor speed control. An 8086 reads a potentiometer through an ADC0808 and adjusts the motor's PWM drive according to the converted digital value.

## Project overview

This project demonstrates how an 8086 system can interface with peripheral devices to control a DC motor. The potentiometer provides the speed command. The ADC0808 converts its analog voltage to an 8-bit digital value, and the system uses that value to adjust the PWM duty cycle. An L298 motor driver supplies the motor drive stage.

The accompanying report describes this component arrangement:

- **8086 microprocessor:** coordinates input conversion and motor speed control.
- **8255 Programmable Peripheral Interface (PPI):** connects control signals, ADC data, and status signals to the processor.
- **8253 Programmable Interval Timer (PIT):** provides timing and pulse generation used for PWM control.
- **ADC0808:** converts the potentiometer's analog voltage to digital data.
- **L298 motor driver:** drives the DC motor using the control signal.
- **Potentiometer:** lets the user vary the requested motor speed.
- **Push button:** restarts or triggers an ADC conversion cycle, as described in the report.

## How it works

1. Initialize the PPI and timer peripherals.
2. Start an ADC0808 conversion of the potentiometer voltage.
3. Monitor the ADC's end-of-conversion status and read the digital result.
4. Use the result to set the timer count and PWM duty cycle.
5. Drive the motor through the L298 and repeat to respond to user input.

## Project files

- `2010040.pdsprj` — Proteus Design Suite project file containing the circuit design.
- `2010040.pdf` — project report, including the design description, assembly code, circuit illustration, results, and references.

## Opening the project

Open `2010040.pdsprj` in Proteus Design Suite. The project was supplied with the report and demonstration video. The report describes the intended circuit and system behavior; consult it alongside the Proteus design when reviewing the implementation.

## Course context

Prepared for **ECE 3111: Microprocessor, Assembly Language & Interfacing**, Department of Electrical & Computer Engineering, Rajshahi University of Engineering & Technology.

## Author

**Puja Roy Dipa**  
Roll: 2010040  
Session: 2020–2021

## Notes

This repository documents an academic project. The report describes the design and reported outcomes; results may depend on the Proteus version, circuit configuration, and simulation setup.
