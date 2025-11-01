🌱 Smart Microgreen Farming Platform
AI-Driven Light Recipe Control for Urban Agriculture
A human–AI collaborative farming platform.

📌 Overview
This project presents a modular, low-cost, and intelligent plant farming system designed for use in space-constrained urban settings, such as condominiums. The system integrates:
Spectrum-adjustable grow lights
Automated irrigation and ventilation
Environmental sensing
Edge AI for light recipe generation
Time-lapse–based growth monitoring
The project demonstrates how AI can co-design and co-operate with humans to create an autonomous microgreen farming solution using commercially available components in Thailand.

## 🏗 System Architecture
The micro-farm is structured as a **three-layer CPS** (Figure 1 in the paper):

| Layer | Function | Hardware / Tools |
|-------|-----------|------------------|
| **Edge** | Real-time sensing & actuation | ESP32 (Smart Farm V1 Plus), RP2040 light driver |
| **Fog** | Local AI inference & contextual reasoning | Raspberry Pi 5 (Python 3.11 + MQTT) |
| **Cloud** | Long-term analytics & model retraining | Remote server / Colab / local PC |

- The **ESP32** manages soil moisture, temperature, humidity, and irrigation/fan control.  
- The **RP2040** provides **6-channel PWM lighting** for spectral tuning (Red 660 nm, Blue 450 nm, Violet 405 nm, Green, Yellow, White).  
- The **Raspberry Pi 5** hosts the **Edge-AI inference engine**, camera acquisition, and MQTT broker for low-latency coordination.  
Latency between sensing and actuation is **< 200 ms**, ensuring responsive environmental control:contentReference[oaicite:3]{index=3}.

---

## 🔩 Hardware Design
The cultivation unit is a **50 × 40 × 60 cm vertical frame** suitable for condominium balconies or kitchen counters.  
Major subsystems:

- **3D-printed modular frame** with integrated cable channels  
- **Spectrum-adjustable LED bar** on aluminum heatsink + acrylic diffuser  
- **Soil moisture & temperature probe (RS-485)**  
- **SHT31 Temp/RH sensor** and **BH1750 light sensor**  
- **Raspberry Pi Camera** capturing hourly growth images  
- **Mist generator**, **fan**, and **solenoid pump** for closed-loop climate regulation  
- Single **12 V DC power supply** with isolated outputs for digital and electromechanical circuits  

All components are **locally sourced in Thailand** (Gravitech, INEX, ArduinoAll) to ensure affordability and replicability:contentReference[oaicite:4]{index=4}.

---
