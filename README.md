# 🔥 Autonomous Fire Detection Robot (ROS 2 + YOLOv5)

An autonomous robotic system designed to detect fire in real-time using computer vision and deep learning. The robot operates in a simulated warehouse-like environment, continuously monitoring surroundings using a camera and detecting fire using a YOLOv5 model.

---

## 📌 Project Description

Fire accidents in warehouses can cause severe damage due to the presence of flammable materials. This project presents an intelligent robotic solution that autonomously patrols an environment and detects fire early using AI. The system combines robotics, simulation, and deep learning to improve safety and reduce human risk.

---

## ⚙️ How the System Works

1. The robot moves inside a simulated environment using predefined motion commands.
2. A camera mounted on the robot captures real-time video frames.
3. These frames are published over a ROS 2 topic (`/rgb_cam/image_raw`).
4. A detection node subscribes to this topic and processes each frame.
5. The YOLOv5 model analyzes the image and detects fire.
6. If confidence > 60%:
   - A bounding box is drawn
   - An alert message is triggered

The system runs asynchronously, meaning movement and detection happen simultaneously without blocking each other.

---

## 🚀 Features

- 🔄 Real-time fire detection using YOLOv5
- 🤖 Autonomous robot movement in simulation
- 📡 ROS 2-based modular communication
- 🌍 3D simulation using Gazebo
- 🎯 Bounding box visualization and alert system
- ⚡ Parallel processing (navigation + detection)

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
├── yolobot_description/   # Robot model (URDF)
├── yolobot_gazebo/       # Simulation world
├── yolobot_control/      # Movement logic
├── yolobot_recognition/  # Fire detection (YOLOv5)

---

## ▶️ How to Run

### 🔹 1. Setup Workspace
```bash
cd ~/ROS/Autonomous-robot-for-fire-detection
colcon build
source install/setup.bash
```

---

### 🔹 2. Launch Simulation & Control Node
```bash
ros2 launch yolobot_gazebo yolobot_launch.py
```

---

### 🔹 3. Run Detection Node
```bash
cd ~/ROS/Autonomous-robot-for-fire-detection
source install/setup.bash
cd src/yolobot_recognition/scripts
python3 ros_recognition_yolo.py
```

---

## 📊 Results

- Accurate real-time fire detection
- Smooth robot navigation
- Reliable ROS2 communication
- Reduced false detections using confidence threshold

---

## ⚠️ Challenges

- Integration of YOLOv5 with ROS2 pipeline  
- Crashes in Gazebo and RViz  
- Tuning detection confidence  
- Debugging ROS2 communication  

---

## 🔮 Future Improvements

- Add SLAM for autonomous navigation
- Integrate thermal sensors
- Deploy on real robot hardware
- Add fire suppression mechanism
