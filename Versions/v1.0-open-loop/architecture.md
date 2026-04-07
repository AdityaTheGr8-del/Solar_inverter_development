# v1.0 — Open Loop Low Power Inverter

## Overview
This version is a basic open-loop inverter designed to convert 12V DC to AC output using PWM switching. No feedback control is used.

---

## Specifications

Input Voltage: 12V DC  
Output Voltage: ~230V AC (approx)  
Waveform: Square wave  
Control: Open loop  
Switching Frequency: 31.4 kHz  
Topology: H-Bridge  

---

## Architecture

Battery (12V DC)  
→ Gate Driver (IR2104)  
→ MOSFET H-Bridge  
→ Step-up Transformer  
→ AC Output  

---

## Controller

Microcontroller: Arduino  
PWM generation: Yes  
Deadtime: To be added  

---

## Gate Driver

IC: IR2104  
High side + Low side driver  
Bootstrap based high side switching  

---

## Power Stage

MOSFET: IRFZ44N (planned)  
Configuration: Full bridge  
Transformer: 12-0-12 to 230V  

---

## Control Type

Open loop  
No voltage sensing  
Output depends on duty cycle  

---

## Limitations

No voltage regulation  
Output varies with load  
Square wave output  
No protection circuit  

---

## Goal of v1.0

Validate switching  
Test driver circuit  
Generate AC output  
Verify transformer operation  
