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

🔧 Hardware Components
All components were selected based on local availability and cost-effectiveness in Southeast Asia. The system includes:
Component	Description
-  Raspberry Pi	Edge controller, camera & image processing
-  ESP32	Sensor and actuator control (MicroPython)
- Grow Light Assembly	6-channel spectrum-adjustable LED array
- RS485 Soil Sensor	Moisture sensing
- SHT31, BH1750	Temp, humidity, and light sensing
- Mist Nozzles + Solenoids	Automated fog and watering
- Pi Camera	Image capture every hour

🌿 Dataset Overview: AI-Assisted Microgreen Cultivation
This data repository supports the development of a smart microgreen farming platform by integrating sensor data acquisition, visual monitoring, and AI-assisted control. In this experiment, microgreens are cultivated under controlled indoor conditions, and a suite of sensors continuously monitors soil moisture, air temperature, relative humidity, and ambient light intensity. Simultaneously, a camera module captures real-scene time-lapse images of plant growth at hourly intervals.
The collected multimodal data are then analyzed by an AI model, which generates adaptive control strategies—specifically tailored light recipes, watering intervals, and mist cycles—based on both environmental feedback and growth stage classification. This human–AI collaborative workflow enables a dynamic and data-driven approach to urban farming, optimizing resource use and enhancing crop yield within compact living spaces.
