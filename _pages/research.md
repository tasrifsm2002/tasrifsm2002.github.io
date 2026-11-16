---
layout: page
permalink: /research/
title: Research
description: Spintronic devices and circuits for energy-efficient, brain-inspired computing hardware.
nav: true
nav_order: 2
---

My research sits at the interface of device physics and circuit design for post-CMOS hardware. I am especially interested in how spintronic devices and two-dimensional materials can be combined into energy-efficient, hardware-intrinsic building blocks for neuromorphic computing.

## Undergraduate thesis: GHz-range PWM generation with a spin Hall nano-oscillator

_Voltage Controlled High-Frequency Pulse Width Modulation Generation based on Spin Hall Nano-Oscillator_ — supervised by [Dr. Orchi Hassan](https://orchi.buet.ac.bd), Dept. of EEE, BUET. Defended June 2026.

### The problem

Conventional CMOS-only pulse-width-modulation (PWM) generators hit performance ceilings in the GHz regime: parasitic capacitance, unfavourable power scaling with frequency, and degraded timing resolution all follow from the physics of charge transport and cannot be fixed by process scaling alone. Yet GHz-range PWM signals are needed for advanced RF transmitters, neuromorphic computing engines, and miniaturised power converters for next-generation embedded systems.

### Approach

The thesis replaces the high-speed digital oscillator with a field-free **Spin Hall Nano-Oscillator (SHNO)**. Spin-orbit torque sustains natural GHz-range magnetization precession in a magnetic tunnel junction (MTJ) without an external magnetic field. The precessing magnetization modulates the MTJ resistance quasi-sinusoidally; a resistive voltage divider turns this into a voltage signal, which a three-stage FinFET CMOS inverter chain digitises into a rail-to-rail square wave.

Two circuit architectures were designed, simulated and compared in HSPICE, using a macrospin LLGS-based MTJ model and Predictive Technology Model (PTM) FinFET cards:

1. **7T-1MTJ design** — a single p-channel FinFET acts as the voltage-controlled series resistance in the divider.
2. **Transmission-gate variant** — the single pFET is replaced by a CMOS transmission gate (an nFET and pFET in parallel with complementary control signals), which gives a much flatter on-resistance versus control-voltage characteristic.

### Results

- **7.5 GHz** oscillation, **6–95% duty-cycle tuning**, and total average power **below 50 µW** for the 7T-1MTJ design.
- Oscillation frequency and duty cycle are fully decoupled: changing the gate-source voltage V<sub>SG</sub> does not change the oscillator frequency.
- The transmission-gate variant improves linearity (R² > 0.98 over a 20–85% duty-cycle range) with about **4× lower control sensitivity** (~1.5%/mV versus ~6%/mV), with power remaining in the same microwatt regime.
- To the best of my knowledge, this is the first PWM generator that simultaneously achieves GHz-range oscillation and sub-50 µW power consumption.

**Keywords:** pulse width modulation, spin Hall nano-oscillator, magnetic tunnel junction, spin-orbit torque, FinFET, duty-cycle control, spintronic-CMOS hybrid circuit, HSPICE, LLGS equation.

The full abstract is on the [publications](/publications/) page.

## Ongoing work: spintronic non-volatile memory and 2D materials

I am investigating spin-transfer torque (STT) and spin-orbit torque (SOT) switching mechanisms in magnetic tunnel junctions for next-generation non-volatile memory architectures, and extending this work toward two-dimensional material platforms — modelling memristive and spintronic device behaviour for synaptic and neuronal emulation in neuromorphic hardware.

## Looking ahead

I am open to research opportunities and collaborations on novel materials and device physics for next-generation computing hardware. If this overlaps with your work, please get in touch at [mahmud.tasrif@bracu.ac.bd](mailto:mahmud.tasrif@bracu.ac.bd). For my background, see my [CV](/cv/).
