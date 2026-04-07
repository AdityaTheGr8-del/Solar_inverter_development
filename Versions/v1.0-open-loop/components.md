# v1.0 Components

This document lists all components used in version 1.0 and the reason for selecting them.

---

## Gate Driver IC

Component: IR2104  
Type: Half Bridge Gate Driver  

Why Used:
- Can drive high-side and low-side MOSFETs  
- Bootstrap based high-side driving  
- Simple interface with microcontroller  
- Suitable for low power inverter  

Alternatives Considered:
- IR2110 (rejected — more complex)
- Discrete transistor driver (rejected — unstable)

Risk:
Bootstrap capacitor sizing critical  
High side duty cycle limitations  

---

## MOSFET

Component: IRFZ44N  
Type: N Channel Power MOSFET  

Why Used:
- Easily available  
- Logic level compatible  
- Suitable for low voltage inverter  
- Low cost  

Alternatives Considered:
- IRF3205
- IRLZ44N

Risk:
Heating at high current  
Requires proper gate drive voltage  

---

## Transformer

Type: Step-up transformer  
Rating: 12-0-12 to 230V  

Why Used:
- Convert low voltage DC switching to high voltage AC  
- Simple inverter topology  
- Easily available  

Risk:
Losses  
Voltage drop under load  

---

## Microcontroller

Component: Arduino  

Why Used:
- Easy PWM generation  
- Quick prototyping  
- Flexible frequency control  

Risk:
No hardware deadtime  
Timing accuracy limited  

---

## Passive Components

Bootstrap Capacitor  
Gate Resistor  
Pull-down Resistor  

Why Used:
Driver stability  
MOSFET protection  
Noise reduction  
