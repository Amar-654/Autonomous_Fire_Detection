# 🔥 Autonomous Fire Detection Robot (ROS 2 + YOLOv5)

An autonomous robotic system designed to detect fire in real-time using computer vision and deep learning. The robot operates in a simulated environment and continuously monitors surroundings using a camera, detecting fire using a YOLOv5 model.

---

## 📌 Overview

This project integrates robotics, simulation, and AI to build a fire detection system. The robot patrols an environment, captures live camera data, and processes it using a deep learning model to identify fire and trigger alerts.

---

## 🚀 Features

- 🔄 Real-time fire detection using YOLOv5
- 🤖 Autonomous robot movement in simulation
- 📡 ROS 2-based modular communication
- 🌍 3D simulation using Gazebo
- 🎯 Bounding box visualization and alert system
- ⚡ Asynchronous processing (movement + detection)

---

## 🛠️ Tech Stack

- ROS 2 (Jazzy)
- Gazebo (Harmonic)
- YOLOv5
- PyTorch
- OpenCV
- cv_bridge
- Python

---

## 📂 Project Structure

src/
├── yolobot_description/
├── yolobot_gazebo/
├── yolobot_control/
├── yolobot_recognition/

---

## ▶️ How to Run

1. Setup workspace
2. Launch simulation
3. Run control node
4. Run detection node

---

## 🎯 Results

- Real-time fire detection
- Smooth robot navigation
- Reliable ROS2 communication

---

## 👨‍💻 Author

Abhishek Patil
