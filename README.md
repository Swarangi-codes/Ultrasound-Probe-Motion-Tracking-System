# Real-Time Ultrasound Probe Motion Tracking System

## 🚀 Overview
Developed a **real-time 6-DoF motion tracking system** for ultrasound probes to estimate **position, orientation, and trajectory** with high accuracy.

Ultrasound imaging is inherently **operator-dependent**, where probe motion directly impacts image quality. This project addresses that limitation by enabling **quantitative tracking and analysis of probe movement**, paving the way for standardization and automation.

---

## 🎯 Objectives
- Track **probe pose (position + orientation)** in real-time  
- Fuse **IMU + vision-based measurements** for robust estimation  
- Provide **trajectory visualization and motion metrics**  
- Enable applications in **robotic ultrasound and training systems**

---

## 🧠 System Architecture

### 🔧 Hardware Setup
- **BNO085 IMU (9-DoF)** for orientation and motion sensing  
- **ESP32** for real-time data acquisition and transmission  
- **USB Camera** for vision-based tracking using ArUco markers  
- **Custom 3D-Printed Probe** with integrated electronics  
- **Dodecahedron Marker Mount** for multi-angle detection  

---

### 📊 System Pipeline

![System Pipeline](./assets/system_pipeline.png)

> Replace with your PDF diagram showing IMU + Camera → EKF → Output

---

### 📐 Probe Design

![Probe CAD](./assets/probe_design.png)

> Add CAD + final prototype images from your report

---

## ⚙️ Methodology

### Multi-Sensor Fusion
- **IMU Data (100 Hz)** → Orientation (quaternions), angular velocity  
- **Camera Data (20 Hz)** → Pose estimation via ArUco markers  
- **Extended Kalman Filter (EKF)** → Sensor fusion  

---

### 📉 Sensor Fusion Flow

![EKF Flow](./assets/ekf_flow.png)

> Add your EKF/data-flow diagram here

---

### 📈 Output
- Fused **Roll, Pitch, Yaw**
- Real-time **trajectory tracking**
- Motion quality metrics:
  - Stability  
  - Smoothness  
  - Intent  

---

## 📊 Visualization

![Trajectory Visualization](./assets/trajectory_plot.png)

> Add Matplotlib output screenshot from your demo

- Real-time plotting using **Python (Matplotlib)**
- Continuous trajectory + pose updates

---

## 💡 Key Engineering Highlights
- Designed a **low-latency wired data pipeline** using ESP32  
- Implemented **real-time EKF sensor fusion**  
- Built a **modular tracking system** combining inertial + vision sensing  
- Achieved **robust pose estimation despite differing sensor rates**  

---

## 🌍 Applications

### 🤖 Robotic Ultrasound
- Closed-loop control using real-time pose feedback  
- Teleoperation via motion replication  

### 🩺 Image-Guided Procedures
- Needle trajectory planning  
- Accurate targeting for biopsies  

### 🧬 CT/MRI Fusion
- Real-time alignment with pre-acquired scans  
- Multi-modal visualization  

### 🎓 Ultrasound Training
- Motion benchmarking against experts  
- Quantitative skill evaluation  

---

## 🔮 Future Work
- 3D patient model + probe visualization  
- Contact sensing for surface detection  
- Haptic feedback integration  
- GPU acceleration for real-time processing  
- End-to-end clinical validation  

---

## 👥 Team
- **Tanay Kanduri** — Software & Hardware  
- **Digvijay Pundir** — Design & Hardware  
- **Swarangi Kale** — Hardware & Software  

**Mentor:** Dr. Lokesh Basavarajappa  
**Coordinator:** Shivam Kushwah  

---

## 📄 Documentation
📌 Detailed report included in this repository covering:
- Design decisions  
- Hardware integration  
- EKF implementation  
- Experimental insights  

---

## 📌 Setup for Images
1. Create a folder named `assets` in your repository  
2. Add images exported from your report:
