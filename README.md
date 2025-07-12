
# 👁️‍🗨️ Virtual Reality Navigation Assistant for the Visually Impaired

## 📌 Introduction

Navigating unfamiliar environments can be extremely challenging for visually impaired individuals, often impacting their independence and quality of life. While traditional aids like canes and guide dogs are helpful, they have limitations in dynamic and crowded spaces.

This project introduces a **Virtual Reality Navigation Assistant**, an IoT-based solution that utilizes ultrasonic and LiDAR sensors, GPS tracking, and auditory feedback to help visually impaired users detect obstacles and navigate in real-time.

---

## 📚 Literature Review

Research has explored several assistive approaches, such as:
- Wearable sensor-based haptic devices.
- Computer vision-powered obstacle detection.
- VR-enhanced navigation aids for improved spatial awareness.

However, these solutions often lack in robustness or accessibility. This project bridges that gap with a more reliable and user-friendly system.

---

## 🛠️ System Design

### 🔩 Hardware Components
- **Arduino Uno** – Central control unit.
- **Ultrasonic Sensor (HC-SR04)** – Detects nearby obstacles.
- **LiDAR Sensor (simulated using HC-SR04)** – For precise distance mapping.
- **GPS Module** – Tracks real-time location.
- **MPU6050** – Monitors orientation and motion.
- **Buzzer** – Audio alerts for immediate obstacles.
- **DFPlayer Mini + Speaker** – Voice guidance and system feedback.

### 🧠 Software Architecture
- Arduino-based C++ code processes sensor data.
- Integrates GPS parsing (TinyGPS++) and audio feedback.
- Real-time alerts based on threshold distance values.
- Displays sensor and GPS data via Serial Monitor for debugging.

---

## 💻 Implementation

### Arduino Features:
- Obstacle detection using ultrasonic and simulated LiDAR.
- GPS location tracking via `TinyGPS++`.
- Voice feedback using DFPlayer Mini.
- Inertial tracking via MPU6050 for enhanced motion sensing.

### Sensor Integration:
- All sensors are read at regular intervals.
- Obstacle feedback is delivered when object is within 20 cm.
- Voice alert and buzzer notify the user instantly.

---

## 🧪 Testing and Evaluation

### Performance Metrics:
- **Accuracy**: Reliable detection of obstacles via ultrasonic + LiDAR.
- **Latency**: Near real-time response for detection and feedback.
- **Range**: Detection accuracy tested in controlled and real-world scenarios.

### User Feedback:
- Tested with visually impaired individuals for usability and comfort.
- Feedback gathered to refine speech volume, delay, and alerts.

---

## ✅ Results & Discussion

### Strengths:
- ✔️ High precision using LiDAR and ultrasonic combo.
- ✔️ Real-time auditory feedback.
- ✔️ Simple and intuitive to use.
- ✔️ Accessible interface.

### Limitations:
- ⚠️ Ultrasonic sensors may struggle with soft materials.
- ⚠️ Weather and environmental interference.
- ⚠️ Limited battery runtime.
- ⚠️ LiDAR increases hardware cost.

---

## 🔄 Future Enhancements
- Add ML-based obstacle classification.
- Develop a companion **mobile app** for route monitoring.
- Improve battery efficiency and waterproofing.
- Collaborate with NGOs and end-users for continuous feedback.

---

## 📈 Flow Diagram
```text
Sensor Detection → GPS Tracking → Data Processing → Feedback Delivery → User Interaction → Navigation Assistance → Testing & Evaluation → Refinement
```

---

## 🧾 Project Folder Structure
```
├── Arduino_Code.ino
├── README.md
├── /images
│   └── flow-diagram.png
├── /docs
│   └── literature-review.pdf
```

---

## 🔌 Libraries Used
- `Wire.h` – I2C communication.
- `MPU6050.h` – IMU control.
- `SoftwareSerial.h` – Serial comms for GPS and DFPlayer.
- `DFRobotDFPlayerMini.h` – MP3 playback.
- `TinyGPS++` – GPS data parsing.

---

## 🧑‍💻 Getting Started

### Requirements:
- Arduino IDE
- Arduino Uno Board
- HC-SR04 (x2)
- MPU6050
- DFPlayer Mini
- GPS Module (e.g., NEO-6M)

### Setup:
1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/virtual-reality-navigation-assistant
   cd virtual-reality-navigation-assistant
   ```
2. Open the `Arduino_Code.ino` file in the Arduino IDE.
3. Upload to Arduino Uno.
4. Connect sensors and modules as per pin mapping in code.
5. Power on the system and begin navigation.

---

## 📸 Demo & Screenshots

_Add pictures of your setup, real-time testing, and the user interface (optional)._

---

## 📃 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Acknowledgements

Special thanks to:
- The visually impaired participants who tested the system.
- Open-source contributors behind the libraries used.
- Research community for the foundational literature.
