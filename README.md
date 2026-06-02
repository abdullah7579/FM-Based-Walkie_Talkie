# Wireless Voice Transmission and Analysis System

This repository details the complete engineering pipeline for a hardware-level wireless communication system designed to transmit and receive human voice signals. The prototype features discrete analog modulation circuitry and utilizes automated digital signal processing to track system integrity from microphone input to acoustic speaker output.

## Core Architecture & Hardware Specifications
* **Voice Input Pre-Amplification:** Employs a microphone capture stage coupled with an active 2N3904 NPN transistor configuration to optimize low-level baseband signals (300 Hz to 3.4 kHz).
* **75 MHz Modulator & Transmitter:** Generates a high-frequency 75 MHz carrier using dual-stage 2N3904 NPN transistors biased in the active region and regulated by an LC tank oscillator circuit.
* **Tuned Demodulator & Receiver:** Utilizes a frontline LC tuning stage and antenna to filter out-of-band noise and capture the target 75 MHz wave via air transmission.
* **Envelope Detector & Audio Amp:** Extracts the baseband audio envelope through a low-pass filter capacitor and steps up signal power via an LM386 operational amplifier.
* **Real-Time Data Acquisition:** Interfaces the receiver output simultaneously to a 5W output speaker and a workstation soundcard via an auxiliary cable connection.

## Signal Processing & Verification
To validate communication integrity, raw transmitted and received audio envelopes are systematically digitized and evaluated:
* **Time-Domain Verification:** Plots distinct voltage-amplitude fluctuations against elapsed time to visually ensure structural envelope retention.
* **Frequency-Domain Spectral Analysis:** Applies Fast Fourier Transforms (FFT) to generate power spectrum curves, mapping human speech concentrations.
* **Channel Noise Analysis:** Quantifies attenuation, noise floor elevations, and harmonic distortions introduced by the analog wireless channel.
