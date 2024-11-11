# 📡 Radio Signal Processing Module

This module processes radio signals emitted by lizards to identify their species (Elgaria or Cophotis).

---

## 🛠️ **Hardware Design**
### **Reception**
- **Inductor (100mH):** Chosen as the receiver for its reliability at reasonable distances from the lizard.
- Detected pronounced voltage fluctuations that varied with distance, indicating signal reliability.

### **Signal Processing Stages**
1. **Band-pass Filter**:
   - Filters out signals around 89 kHz, which are amplitude modulated with 120 Hz and 200 Hz.
   - Inductance: 2.2mH, Capacitance: 1.5nF.
2. **Non-inverting Amplifier**:
   - Amplifies the signal while maintaining its integrity.
   - Operational Amplifier: LM4562 (Gain-bandwidth product: 55MHz).
   - DC Bias Voltage: 1.65V, AC Gain: ~200x.
3. **Envelope Detector**:
   - Demodulates the signal to retrieve the original frequency before modulation.
   - Resistor: 5 kΩ, Capacitance: 500nF.
4. **Comparator**:
   - Enhances detection range and accuracy while reducing noise.
   - Operates in open-loop mode with a low-pass filter for DC component stabilization.

### **Final Circuit**
- Components are integrated onto a Printed Circuit Board (PCB) for a lightweight design.
- Successfully tested and validated to read radio signals emitted by the lizard.

---

## 🖥️ **Software Integration**
- Converts the processed analog signal into digital output for further analysis.
- Ensures stable and accurate frequency identification.

---

## 📊 **Test Results**
- Successfully identified species-specific signals and achieved accurate detection in controlled tests.

---

## 🖼️ **LTSpice Circuit**
Below is the LTSpice circuit for the Radio Signal Processing module:

![Radio Signal LTSpice Circuit](../../Images/radio_signal_circuit.png)
