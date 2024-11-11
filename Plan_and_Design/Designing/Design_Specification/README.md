# 🛠️ Project Design

The team aimed to build a compact and lightweight rover with dimensions of **25cm × 25cm × 15cm (length × width × height)** and a weight of less than **750g**, as shown in Figure 2 below.

---

## 🖼️ Final Design
<img src="EEE_Rover_Project/Plan_and_Design/Images/rover_front.png" alt="Final Design of the Rover" width="400"/>

*Figure 2: Final design of the rover.*

---

## 🔍 Design Specification
The design specifications for the rover consider various aspects, such as **accuracy**, **reliability**, and **safety**.

### **Accuracy**
- **Hardware**: Components must accurately capture relevant signals within a millisecond and produce stable digital signals for the microcontroller.
- **Software**: Each submodule must not exceed **8%** of the total memory space available in the microcontroller.
- The rover must:
  - Respond to user requests within **1 millisecond**.
  - Move at a minimum speed of **30cm/s**.
  - Stop immediately upon request.

### **Reliability**
- The rover must maintain similar performance for at least **20 minutes** of continuous operation.

### **User Interface**
- Designed to be intuitive, allowing users to maneuver the rover and view data with minimal training.

### **Safety**
- All electrical components, such as batteries and circuits, are safely enclosed and isolated to prevent:
  - **Electrocution**.
  - **Short circuits**.

---

## ⚙️ Lightweight and Compact Design
To ensure a lightweight and compact rover:
- The chassis was **3D printed** using polylactic acid (PLA).
- Printed Circuit Boards (PCBs) and stripboards were designed for all sub-module circuits to minimize weight and size.
- The design avoids disturbing shy lizards by keeping the total weight below **750g**.
