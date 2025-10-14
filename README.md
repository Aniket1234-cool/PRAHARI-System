# 🛡️ PRAHARI  
### **Protective Robotic Aerial High-Altitude Response Initiative**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Smart India Hackathon](https://img.shields.io/badge/Smart%20India%20Hackathon-2025-orange.svg)](#)
[![Build Status](https://img.shields.io/badge/Status-Prototype%20Ready-green.svg)](#)
[![Platform](https://img.shields.io/badge/Platform-Jetson%20%7C%20Python%20%7C%20ROS%20%7C%20CoppeliaSim-blue.svg)](#)

---

> **PRAHARI** is an intelligent, modular counter-drone platform designed for **high-altitude defense and border security**.  
Developed for **Smart India Hackathon 2025**, the system fuses **AI-powered robotics**, **vision intelligence**, and **software-defined radio** to deliver a **multi-layered autonomous defense** against aerial threats.

---

## 🎥 Quick Demo / Overview Video    

<iframe width="560" height="315" src="https://www.youtube.com/embed/mN3kXhBsl9o?rel=0" 
frameborder="0" allowfullscreen></iframe>

---

## 🚀 Key Features

### 🧠 AI-Driven Vision

* YOLOv8-based object detection for **real-time drone recognition**.
* External Python vision pipeline using **sensor fusion** (RGB + depth + IR).

### 🤖 Robotic Arm Automation

* 6-DOF arm (Niryo simulated / hardware ready).
* **Reinforcement Learning (RL)** module for **predictive tracking and smooth interception**.
* Adaptive servo and stepper control for accurate pointing and neutralization.

### 📡 Multi-Layered Communication

* Distributed **LoRaWAN** mesh for low-power, long-range alerts.
* Reliable operation in **rugged, high-altitude environments**.

### 🔒 Soft-Kill Defense Stack

* **SDR-based jamming** and **GNSS spoofing** for drone neutralization.
* Optional **friend-drone counter-offensive coordination** via mesh.

### 🧩 Modular & Scalable Architecture

* Plug-and-play design enabling rapid reconfiguration.
* Ruggedized, **field-deployable** hardware enclosures.
* **CoppeliaSim integration** for hybrid simulated + physical testing.

---

## 🗂️ Repository Structure

```
PRAHARI/
│
├── vision/                      # YOLOv8 and sensor data fusion
│   ├── yolov8/
│   └── utils/
│
├── reinforcement_learning/      # RL training and policy deployment
│   ├── training/
│   └── control_interface/
│
├── simulation/                  # CoppeliaSim scenes and models
│   └── niryo_drone_scene.ttt
│
├── hardware/                    # 3D printable parts, circuit diagrams
│
├── docs/                        # System architecture, design guides
│
├── config/                      # LoRaWAN and AI parameters
│
├── tests/                       # Unit and integration tests
│
└── requirements.txt
```

---

## ⚡ Quick Start

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/<your-org>/PRAHARI.git
cd PRAHARI
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
cd vision/yolov8
pip install -r requirements.txt
```

### 3️⃣ Start Simulation

* Open the `.ttt` files in **CoppeliaSim**.
* Launch vision streaming:

  ```bash
  python vision/utils/sensor_data_pull.py
  ```

### 4️⃣ Run YOLOv8 Detection

```bash
python vision/yolov8/yolov8_inference.py --source path_to_sensor_data
```

### 5️⃣ Train the RL Policy

```bash
python reinforcement_learning/training/train_policy.py
```

---

## 🧭 Development Roadmap

| Phase       | Description                                              | Status         |
| ----------- | -------------------------------------------------------- | -------------- |
| **Phase 1** | Simulation + AI Integration (Niryo Arm + Drone + YOLOv8) | ✅ Completed    |
| **Phase 2** | Hardware Design and preliminary integration              | 🧩 In Progress |
| **Phase 3** | Jetson Nano hardware deployment with LoRaWAN mesh        | 🚧 Planned     |
| **Phase 4** | SDR jamming + Vajra interceptor integration              | 🚧 Planned      |
| **Phase 5** | Field validation and full-scale testing                  | ⏳ Pending      |

---

## 📘 Documentation

* **System Architecture** → `docs/architecture_overview.md`
* **Hardware Configuration** → `hardware/`
* **Simulation Setup** → `simulation/`
* **AI & RL Modules** → `vision/` and `reinforcement_learning/`

---

## 🤝 Contributing

We welcome research and academic collaborations!

1. Fork this repository
2. Create a feature branch (`feature/<module>`)
3. Submit a pull request following [CONTRIBUTING.md](CONTRIBUTING.md)

---

## ⚖️ License

Released under the **MIT License**.
Hardware and simulation assets are open for **research and academic use** only.
© 2025 Aniket Mandal & Team TECHNOVATORS

---

> **PRAHARI — Autonomous protection for the skies above our borders.**
> *Engineered for reliability. Designed for resilience.*

