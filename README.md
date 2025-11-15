# Intelligent Traffic Signal Control Using Real-Time Traffic Density Detection

This project presents a **real-time adaptive traffic signal control system** that uses CCTV footage to analyze vehicle density at traffic junctions. By leveraging **image processing** and **object detection**, the system dynamically adjusts traffic signal timings to reduce congestion and improve traffic flow efficiency.

The entire system is divided into **three main modules**:

1. **Vehicle Detection Module**
2. **Signal Switching Algorithm**
3. **Traffic Simulation Module**

---

## 1. Vehicle Detection Module

This module receives video input from CCTV cameras installed at traffic junctions.

### Technologies Used

* **OpenCV**
* **NumPy**
* Pretrained object detection models 

### Functionality

* Processes the video frames in real time
* Detects and counts the number of vehicles in each category:

  * Car
  * Bike
  * Bus
  * Truck
* Computes the **traffic density** for each lane based on detected vehicle counts

---

## 2. Adaptive Signal Switching Algorithm

Once density is calculated, the system determines the **optimal green signal duration** for each lane.

### Features

* Dynamically adjusts **green** signal times based on real-time traffic load
* Ensures fair allocation of signal time across lanes
* Maintains **minimum** and **maximum signal duration limits** to avoid starvation of any lane
* Responds to fluctuations in traffic density seamlessly
  
---

## 3. Simulation Module

To evaluate the system’s performance, a simulation environment is implemented.

---

## System Architecture

```
CCTV Camera Feed
        │
        ▼
 Vehicle Detection Module (OpenCV + Object Detection)
        │
        ▼
Traffic Density Computation
        │
        ▼
Adaptive Signal Switching Algorithm
        │
        ▼
 Traffic Light Controller
        │
        ▼
   Simulation Module (Visualization & Comparison)
```

---

## Tech Stack

* **Python**
* **OpenCV**
* **NumPy**
* **Object Detection Models**
* **Pygame / Custom UI** for simulation (depending on your implementation)

---

## How It Works

1. Capture or input a video feed from a traffic camera.
2. Preprocess and detect vehicles in each frame.
3. Count vehicles per lane and calculate density.
4. Feed density into adaptive signal algorithm.
5. Generate optimized signal timings.
6. Visualize and compare with static signal system.

---

## Future Work

* Integrate Deep Learning-based vehicle detection (YOLOv8, Faster R-CNN)
* Handle nighttime/low-light scenarios
* Deploy on embedded systems (Jetson, Raspberry Pi)
* Multi-junction collaborative traffic signal optimization
* Integration with city-wide traffic management systems


