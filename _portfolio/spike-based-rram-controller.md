---
title: "Spike-Based RRAM Memory Controller"
excerpt: |
  <figure class="project-preview">
    <img src="/images/rram-memory-controller.png" alt="RRAM analog-interface simulation, crossbar controller diagram, and waveform">
  </figure>

  Built a Verilog FSM controller for an 8x8 RRAM crossbar on the DE0-Nano FPGA, separating control and pulse-generation clocks. Experimental work redesigned the analog read path and demonstrated sensing from a 5 ns read pulse. IIT Bombay. May 2025 - July 2025.
collection: portfolio
---

This project developed an FPGA-driven controller and analog interface for read/write operations on an 8x8 RRAM crossbar. The digital controller was implemented in Verilog on a DE0-Nano (Cyclone IV) FPGA, with finite-state-machine logic for cell selection and control-pulse sequencing. I verified the RTL in ModelSim and used Quartus Prime for synthesis, timing analysis, and FPGA implementation.

Timing analysis showed that a single clock domain constrained pulse-width resolution, so the design separated the main FSM clock from the faster pulse-generation clock. Experimental work evaluated pulse behavior on the crossbar interface and identified ringing and settling limitations in the analog read path. I then worked on a redesigned sensing stage using a transimpedance amplifier, fast-recovery diode, and peak-detection capacitor; the circuit converted a 5 ns read pulse into a voltage that could be sampled by the ADC.

The work connects FPGA control with analog measurement for non-volatile-memory and neuromorphic-computing systems. The public repository contains the controller RTL and documentation; some laboratory hardware design files are not included because of confidentiality constraints.

<strong>Tools and methods:</strong> Verilog, DE0-Nano, ModelSim, Quartus Prime, finite-state machines, static timing analysis, oscilloscope-based testing, RRAM crossbar control.

[Project repository](https://github.com/USb-dB/5ns-Spike-Based-RRAM-Memory-Controller-)

<figure class="project-preview">
	<img src="/images/rram-memory-controller.png" alt="RRAM controller and analog-interface simulation diagram with measured waveform">
	<figcaption>RRAM controller architecture and analog-interface simulation results.</figcaption>
</figure>