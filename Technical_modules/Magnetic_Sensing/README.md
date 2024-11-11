# 🧲 Magnetic Sensing Module

This module detects magnetic polarity to identify lizard species.

---

## 🛠️ **Hardware Design**
- Measures magnetic field differences between the magnet and Earth.
- Simple comparator circuit implemented for polarity detection.

---

## 🖥️ **Software Integration**
### **Polarity Detection Logic**
- Outputs:
  - **"North Pole"** if the difference > 10.
  - **"South Pole"** if the difference < -10.
  - **"Neutral"** if the difference is between -10 and 10.

