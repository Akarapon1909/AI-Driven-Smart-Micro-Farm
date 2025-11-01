## 🌱 Smart Microgreen Farming Platform
AI-Driven Light Recipe Control for Urban Agriculture
A human–AI collaborative farming platform.

## 📌 Overview
This project presents a modular, low-cost, and intelligent plant farming system designed for use in space-constrained urban settings, such as condominiums. The system integrates:
Spectrum-adjustable grow lights
Automated irrigation and ventilation
Environmental sensing
Edge AI for light recipe generation
Time-lapse–based growth monitoring
The project demonstrates how AI can co-design and co-operate with humans to create an autonomous microgreen farming solution using commercially available components in Thailand.

## 🏗 System Architecture
The micro-farm is structured as a **three-layer CPS** :

| Layer | Function | Hardware / Tools |
|-------|-----------|------------------|
| **Edge** | Real-time sensing & actuation | ESP32 (Smart Farm V1 Plus), RP2040 light driver |
| **Fog** | Local AI inference & contextual reasoning | Raspberry Pi 5 (Python 3.11 + MQTT) |
| **Cloud** | Long-term analytics & model retraining | Remote server / Colab / local PC |

- The **ESP32** manages soil moisture, temperature, humidity, and irrigation/fan control.  
- The **RP2040** provides **6-channel PWM lighting** for spectral tuning (Red 660 nm, Blue 450 nm, Violet 405 nm, Green, Yellow, White).  
- The **Raspberry Pi 5** hosts the **Edge-AI inference engine**, camera acquisition, and MQTT broker for low-latency coordination.  
Latency between sensing and actuation is **< 200 ms**, ensuring responsive environmental control.

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

All components are **locally sourced in Thailand** (Gravitech, INEX, ETT) to ensure affordability and replicability.

---

## 📊 Summary of Data Repository

The AI–Driven Smart Micro-Farm data repository comprises three synchronized datasets acquired during real microgreen cultivation, collectively capturing the full perception–reasoning–actuation cycle of the system.
Together they enable quantitative, visual, and cognitive reconstruction of plant growth and AI decision-making.

Part	Dataset	Core Content	Purpose & Research Use
- ** I	Environmental & Sensor Dataset	Continuous numerical logs of soil temperature and moisture, air temperature and humidity, light intensity, pH, nutrient (NPK) levels, and actuator states collected every minute during 10-day Brassica juncea microgreen cycles.	Provi des the physical layer of the CPS — for control-system validation, environment–growth correlation, and energy-efficiency analysis.
- ** II	Time-Lapse Scene Dataset	Hourly high-resolution images (1920 × 1080 px) of the growth tray captured by the Raspberry Pi camera, synchronized with lighting and sensor data.	Offers the visual layer — supporting phenotypic tracking, color-index (ExG, Hue, Coverage) computation, and AI training for stage classification and canopy analysis.
- ** III	AI Growth-Analysis and Actuation Dialogue Dataset	Daily JSON records summarizing the AI’s perception (sensor + image interpretation), reasoning with literature references, and generated control recommendations (irrigation, humidity, lighting, pH adjustment).	Represents the cognitive layer — enabling explainable-AI studies, rule extraction, and evaluation of adaptive decision quality across growth phases.
