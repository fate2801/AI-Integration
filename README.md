# ✈️ Airplane Motion Detection Smart System

## 📖 Project Overview
This project is an **AI-powered motion detection system for airplanes**, designed to detect and classify motion states in real-time and issue immediate alerts during critical motion events such as turbulence. The system integrates sensors, edge AI, wireless communication, and a remote monitoring dashboard to improve in-flight safety and awareness.

---

## 📑 Features
- 📡 **Real-time motion detection using an accelerometer**
- 🧠 **Edge AI model for motion classification**
- 🚨 **Emergency alert system (LED, Buzzer, OLED display)**
- 🌐 **LoRaWAN communication for long-range data transmission**
- 📊 **Node-RED dashboard for remote monitoring and control**

---

## 🖥️ System Workflow
1. **LIS3DHTR Accelerometer** samples motion data at **100Hz**
2. **ESP32 Microcontroller** reads sensor data and runs a machine learning model (trained with **Edge Impulse AI**) for motion classification:
   - Stable  
   - Left Tilt  
   - Right Tilt  
   - Shaking (Turbulence)
3. On detecting turbulence:
   - **OLED Display** shows `SHAKING`
   - **LED** turns ON
   - **Buzzer** sounds
4. The system sends the motion status via **LoRa E5 Module** to a **LoRa Gateway / The Things Stack**
5. **Node-RED dashboard** visualizes real-time motion data and offers remote system control

---

## 📦 Components Used

### 🔧 Hardware

| Component                | Purpose                         |
|:------------------------|:--------------------------------|
| **ESP32 Microcontroller** | Core processing unit             |
| **LIS3DHTR Accelerometer**| Motion sensing (100Hz sampling) |
| **OLED Display**          | Display motion status            |
| **LED & Buzzer**          | Emergency alerts                 |
| **LoRa E5 Module**        | Long-range communication         |

### 💾 Software

| Tool / Platform          | Purpose                          |
|:------------------------|:---------------------------------|
| **Edge Impulse AI**       | Machine learning model training  |
| **Arduino IDE**           | Programming the ESP32            |
| **Node-RED**              | Dashboard and data visualization |
| **The Things Stack (TTS)**| LoRaWAN network management       |

---

## 📊 Node-RED Dashboard
A clean, interactive dashboard built using **Node-RED** to:
- View real-time motion status
- Log historical data
- Provide downlink control options for remote system management

---

## 📸 Project Poster
This project was summarized in a **final submission poster**, showcasing:
- System workflow
- Hardware setup
- AI classification states
- Remote dashboard interface

---

## 📚 Conclusion
This system demonstrates the practical integration of **Edge AI, wireless IoT communication, and real-time monitoring** for aviation safety applications. It serves as a scalable prototype for smart aircraft safety systems and remote telemetry networks.


