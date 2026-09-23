# Frequency-Converter-with-Real-Time-Display-and-Tuning
A low-cost frequency converter designed to transform AC signals of varying frequencies (50-300 Hz) into a stable, tunable sinusoidal output (30-200 Hz). The system utilizes a full-bridge rectifier, an SG3524-controlled half-bridge inverter, an RC filter, and an Arduino-based real-time LCD interface for frequency monitoring.
# Frequency Converter with Real-Time Display and Tuning

## Overview
This repository contains the design, simulation, and hardware implementation of a cost-effective frequency stabilizer and converter. Developed for the EEE 316 Power Electronics Laboratory at the Bangladesh University of Engineering and Technology (BUET), the system addresses frequency mismatches by converting standard AC signals, such as transforming 50 Hz to 60 Hz or vice versa. It accepts varying input frequencies ranging from 50 Hz to 300 Hz and generates a stable, user-tunable sinusoidal signal ranging from 30 Hz to 200 Hz.

## Key Features
* **Adjustable Output:** Users can dynamically tune the output frequency in real-time using an integrated potentiometer.
* **Live Monitoring:** An Arduino-driven LCD panel displays the output frequency for precise, immediate calibration.
* **Broad Compatibility:** The system is capable of handling various input waveforms, including sinusoidal, rectangular, and triangular signals.
* **Safety Mechanisms:** The circuit employs optocouplers for secure gate pulse separation and incorporates 100k resistors on the MOSFETs to eliminate short-circuit risks.

## System Architecture
* **Full-Bridge Rectifier:** Converts the incoming AC signal into a pulsating DC voltage, utilizing a smoothing capacitor to generate a pure, stable DC signal.
* **Half-Bridge Inverter:** Uses IRF250 MOSFETs and an SG3524 IC to convert the DC voltage back into a square wave AC signal at the targeted frequency.
* **RC Filter:** Smooths the square wave output from the inverter using an RC filter and an inductor (L1) to produce a clean sinusoidal waveform.
* **Display Module:** An Arduino Nano calculates the frequency by measuring high and low pulse durations, outputting the exact frequency to a 16x2 I2C LCD display.

## Hardware Components
* **Controller & Display:** Arduino Nano, 16x2 I2C LCD.
* **Inverter Components:** SG3524 PWM IC, IRF250 MOSFETs (x2), Optocoupler.
* **Passive Components:** Diodes (x6), Potentiometers, and various capacitors and resistors (including the essential 100k MOSFET safety resistors).
* **Estimated Cost:** Approximately 1030 BDT.

## Setup and Usage
1. Connect the AC signal source to the system's input terminals, ensuring proper polarity.
2. Turn on the power supply to activate the frequency converter.
3. Rotate the potentiometer clockwise to increase the output frequency or counterclockwise to decrease it.
4. Monitor the 16x2 LCD display to verify the real-time output frequency.
5. Connect the output terminals to your target load or external circuit.


