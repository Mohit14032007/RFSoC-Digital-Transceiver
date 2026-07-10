# RFSoC-Based Digital Transceiver using PYNQ

A complete hardware-software co-design implementation of a digital transmitter and receiver on the AMD/Xilinx Zynq UltraScale+ RFSoC 4x2 platform.

The project demonstrates signal generation, RF transmission, signal reception, FFT analysis, and RF Data Converter (RFDC) configuration using Python and the PYNQ framework.

---

## Overview

Modern wireless communication systems require high-speed data converters and real-time digital signal processing. The RFSoC platform integrates:

- ARM Cortex-A53 Processing System
- FPGA Programmable Logic
- Multi-GSPS ADCs
- Multi-GSPS DACs
- RF Data Converter (RFDC)

into a single device.

This project implements an end-to-end digital transceiver capable of generating a baseband waveform, transmitting it through the DAC, receiving it through the ADC, and validating the received signal using FFT analysis.

---

## Features

- RFSoC Hardware-Software Co-Design
- Python-based Control using PYNQ
- RFDC Configuration
- DAC and ADC Initialization
- AXI DMA Data Streaming
- Digital Up Conversion
- Digital Down Conversion
- IQ Data Handling
- FFT-Based Frequency Verification
- Real-Time Signal Visualization

---

## Hardware Used

- AMD/Xilinx Zynq UltraScale+ RFSoC 4x2
- ARM Cortex-A53 Processing System
- FPGA Programmable Logic
- Integrated RF Data Converter
- Spectrum Analyzer
- SMA RF Cable

---

## Software Used

- Python
- PYNQ
- Vivado
- NumPy
- SciPy
- Matplotlib

---

## System Architecture

![Architecture](images/block_diagram.png)

The system consists of:

- ARM Processing System
- AXI DMA
- FPGA Programmable Logic
- RF Data Converter
- DAC
- ADC

---

## Data Flow

```text
Python Application
        │
Generate Sine Wave
        │
Allocate DMA Buffer
        │
AXI DMA
        │
Programmable Logic
        │
RF Data Converter
        │
DAC
        │
Analog Signal
        │
Loopback / RF Path
        │
ADC
        │
RF Data Converter
        │
AXI DMA
        │
ARM Processor
        │
FFT Analysis'''


## How to rub
RF Configuration
Parameter	Value
DAC Rate	4915.2 MSPS
ADC Rate	4915.2 MSPS
Carrier Frequency	300 MHz
Baseband Frequency	20 MHz
Interpolation	×16
Decimation	×16
Nyquist Zone	1

How to Run
Clone Repository
git clone https://github.com/yourusername/RFSoC-Digital-Transceiver.git
Copy Files

Copy

design_1.bit
design_1.hwh

to the working directory.

Launch Jupyter
jupyter notebook
Open
sine_wave_loopback.ipynb

Run all cells sequentially.
