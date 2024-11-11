# 🔊 Ultrasound Signal Processing Module

This module processes modulated ultrasonic signals (40kHz) to extract digital data representing lizard names.

---

## 🛠️ **Hardware Design**
### **Amplification**
- **Operational Amplifier:** NE5532 with an inverting amplifier configuration (Gain: -3).
- Bias Voltage: 2.5V using a potential divider.

### **Envelope Detection**
- Removes the negative component of the modulated signal using a diode.
- Ripple voltage reduced with a 10nF capacitor to maintain clear high and low bits.

### **Low-pass Filtering**
- Filters the envelope signal for smoother waveform transitions.
- Produces digital signal (S1 and S2) suitable for microcontroller processing.

### **Comparator**
- Converts analog signals into binary outputs (5V for bit 1, 0V for bit 0).

### **Final Design**
- Integrated onto a lightweight PCB.
- Ultrasonic receiver connected via terminals J1 and J2.

---

## 🖥️ **Software Integration**
### **UART Decoding**
- Processes digital signals into lizard names using the following logic:
  - Recognizes each character as a 2-bit hexadecimal number (reversed bit order).
  - Detects start (0) and stop (1) bits for each character.
  - Ensures stable data transmission at 600 bits per second with a `bitDuration` of 1667 µs.

### **Flowchart**
- Logical flow ensures error-free and stable decoding of lizard names.

---

## 📂 **Files**
- **Circuit Simulation**: `ultrasound_signal.asc` (LTSpice).
- **PCB Layout**: `ultrasound_signal_pcb.pdf`.
