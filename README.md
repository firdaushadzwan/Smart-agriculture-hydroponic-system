# 🌱 HydroSense – Smart Hydroponic Monitoring System

Arduino-based environmental monitoring system for **small-scale hydroponic agriculture**, designed to provide **real-time monitoring of temperature, humidity, and water level**.

This project was developed as part of the **KIG3008 Instrumentation and Measurement Techniques** course in the **Department of Mechanical Engineering**.

HydroSense replaces manual observation with a **sensor-based smart monitoring system**, improving reliability and efficiency in hydroponic farming environments.

---

# 📌 Project Overview

HydroSense is a **low-cost smart agriculture monitoring prototype** that continuously measures important environmental parameters in a hydroponic setup.

The system integrates multiple sensors with an **Arduino-based data acquisition unit** to monitor:

- 🌡 Temperature  
- 💧 Water Level  
- 💨 Relative Humidity  

Sensor data is processed in real-time and displayed through:

- 📟 I2C LCD Display  
- 💡 LED Warning Indicators  
- 💻 Arduino Serial Monitor

The system alerts the user whenever environmental parameters exceed predefined safety thresholds.

---

# 🎯 Project Objectives

- Develop a **smart hydroponic monitoring system** using embedded instrumentation techniques  
- Monitor **temperature, humidity, and water level** in real time  
- Provide **visual alerts when environmental limits are exceeded**  
- Apply **sensor integration, data acquisition, and signal processing concepts**

---

# 🧠 System Architecture

The HydroSense system follows a standard **measurement chain architecture**:

```
Physical Environment
        │
        ▼
     Sensors
(DHT11 & Water Level)
        │
        ▼
   Arduino Uno
 (Data Acquisition)
        │
        ▼
 Data Processing
 (Threshold Logic)
        │
        ▼
 Output Interface
 LCD + LEDs + Serial Monitor
```

---

# 🧰 Hardware Components

| Component | Function |
|--------|--------|
| Arduino Uno | Main controller & data acquisition unit |
| DHT11 Sensor | Measures temperature and humidity |
| Water Level Sensor | Detects water depth |
| I2C LCD Display | Displays real-time sensor readings |
| LEDs | Visual alerts for abnormal conditions |
| Breadboard & Jumper Wires | Prototype circuit connections |

---

# 🔌 Circuit Configuration

| Device | Arduino Pin |
|------|------|
| DHT11 Data | Pin 4 |
| Water Level Sensor | A0 |
| Temperature Alert LED | Pin 8 |
| Humidity Alert LED | Pin 9 |
| Water Level Alert LED | Pin 10 |
| LCD SDA | A4 |
| LCD SCL | A5 |

---

# 💻 Software Implementation

The system software was developed using **Arduino IDE (C++)**.

Main program workflow:

1. Initialize sensors and communication interfaces  
2. Read sensor data continuously  
3. Convert raw sensor data into engineering values  
4. Compare readings with predefined thresholds  
5. Trigger warning LEDs if limits are exceeded  
6. Display data on LCD and Serial Monitor  

Sampling interval: **~2 seconds**

---

# 📊 Example System Responses

| Condition | System Response |
|------|------|
| Normal Environment | All LEDs OFF |
| Temperature > 24°C | Red LED ON + LCD Warning |
| Water Level < 30% | Yellow LED ON + LCD Warning |
| Multiple Faults | Multiple LEDs Activated |

---

# 🧪 Testing & Calibration

The system was tested in a controlled laboratory environment.

Calibration references used:

- Mercury Thermometer (temperature)  
- Graduated Cylinder (water level)  
- Digital Hygrometer (humidity)

Testing scenarios included:

- Baseline operation  
- High temperature simulation  
- Low water level detection  
- Multiple fault conditions  

The system successfully detected abnormal conditions and triggered alerts within **2 seconds response time**.

---

# 📂 Repository Structure

```
HydroSense/
│
├── Arduino_Code/
│     HydroSense.ino
│
├── Circuit_Diagram/
│     wiring_diagram.png
│
├── Images/
│     prototype_setup.jpg
│
├── Documentation/
│     full_project_report.pdf
│
└── README.md
```

---

# 👨‍🔧 My Role – Team Technician

**Position:** Team Technician – Circuit Integration & Arduino Developer

My main responsibilities in this project included:

- Designing and assembling the **circuit connections on the breadboard**
- Integrating sensors, LEDs, LCD display, and Arduino controller
- Developing the **Arduino program for sensor data acquisition**
- Implementing **threshold-based alert logic**
- Debugging hardware connections and stabilizing sensor readings
- Assisting in **hardware–software integration** to ensure system reliability

Through this role, I gained hands-on experience in:

- Embedded systems development  
- Sensor interfacing  
- Real-time data acquisition  
- Circuit troubleshooting  

---

# 📽 Project Demonstration

Project video presentation:

https://youtu.be/My1o_o-VNiw

---

# 👥 Project Team

- Mohamad Firdaus Hadzwan Bin Mohamad Syarul  
- Muhammad Zaim Bin Kamarol Ridzuan  
- Aiman Harisya Bin Zaharudin  
- Wan Muhammad Akram Bin Zahid  
- Izzat Amir Bin Banyami  

Lecturer: **Ts. Dr. Soong Ming Foong**

Department of Mechanical Engineering

---

# 🚀 Future Improvements

Potential enhancements for future development:

- Automatic **pump control system**
- **Wireless IoT monitoring**
- **Cloud data logging**
- Higher precision sensors (DHT22 / SHT series)
- Noise filtering and signal smoothing algorithms

---

⭐ If you find this project useful, feel free to star the repository.
