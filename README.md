# 🚪 Elevator Occupancy Counter Using ESP32-CAM

An AI-powered elevator monitoring system built using the **ESP32-CAM** module to **track the number of people entering and exiting an elevator** in real time. Designed to reduce elevator congestion in high-traffic buildings such as colleges and offices, this project ensures smoother flow and smarter user decisions during peak hours.

---

## 🧩 Project Overview

Elevator congestion is a frequent challenge in high-traffic buildings, where users often encounter elevators that are fully occupied. This leads to **delays**, **inefficient vertical transportation**, and **user frustration**.

This system addresses the issue with an **ESP32-CAM-based Elevator Occupancy Counter** that provides **real-time occupancy tracking** through a live video feed. The data can be used to:
- Monitor occupancy live via browser
- Display current elevator status on a screen in the lobby
- Extend to trigger alerts when capacity is exceeded

By making elevator usage visible and smarter, this solution improves **safety**, **efficiency**, and **decision-making**.

---

## 📌 Features

- 🎥 **Live camera feed** using ESP32-CAM
- 👥 Designed for **entry/exit tracking**
- 🌐 **Web interface** for real-time monitoring
- 📶 Works over **Wi-Fi or mobile hotspot**
- 🔧 Extendable with sensors, ML models, and cloud storage

---

## 🛠️ Hardware Requirements

| Component        | Quantity | Description                            |
|------------------|----------|----------------------------------------|
| ESP32-CAM        | 1        | Camera + microcontroller               |
| FTDI Programmer  | 1        | For uploading code to ESP32-CAM        |
| Jumper Wires     | Several  | To connect FTDI to ESP32-CAM           |
| (Optional) TFT Display | 1 | To display live count in lobby         |
| (Optional) Buzzer     | 1 | Alert on overcapacity                  |

---

## 🔌 FTDI to ESP32-CAM Wiring

| FTDI Pin | ESP32-CAM Pin |
|----------|----------------|
| TX       | U0R (RX)       |
| RX       | U0T (TX)       |
| GND      | GND            |
| 3.3V     | 3.3V           |
| IO0      | GND (only during upload) |

> ⚠️ After code upload, disconnect IO0 from GND before resetting the board.

---

## 🚀 How It Works

1. The ESP32-CAM module runs a camera web server over Wi-Fi or hotspot.
2. Users access the **camera stream via browser** to monitor live activity.
3. (To be integrated) The system can detect **entry/exit** using:
   - Image processing (OpenCV or Edge AI)
   - Motion zones
   - IR/magnetic sensors
4. Occupancy status can be displayed or logged.

---

## 📂 Project Structure

<pre> ```markdown 📂 Project Structure Elevator_Occupancy_Counter/ ├── CameraWebServer_for_prathmesh_hotspot.ino # Main ESP32-CAM sketch ├── app_httpd.cpp # Web streaming logic ├── camera_index.h # HTML/CSS/JS for camera UI ├── camera_pins.h # ESP32-CAM pin config ├── README.md # This documentation ├── description # (Optional placeholder file) └── CameraWebServer_Code/ # Optional extra files or code ``` </pre>

---


## 🔮 Future Enhancements

- 🧠 Add **AI/ML model** to count people via video (OpenCV/Teachable Machine)
- ☁️ Push data to **Firebase / Thingspeak**
- 🖥️ Add **TFT/LCD display** in lobby showing count
- 🔔 Sound **buzzer alert** when maximum capacity is exceeded
- 🧾 Maintain logs with **timestamps** for audit

---


Let me know if you want me to:
- Upload this as a file
- Create a PR to your repo
- Add ML model integration or Firebase guide

Happy building! 🚀
