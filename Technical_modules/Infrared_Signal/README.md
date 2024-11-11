# 🌈 Infrared Signal Processing Module

This module detects and processes infrared signals emitted by lizards to identify their species.

---

## 🛠️ **Hardware Design**
### **Phototransistor Receiver**
- **Component:** EEEBug phototransistor.
- Detects infrared light and converts it into a voltage signal.

### **Signal Filtering**
1. **High-pass Filter**:
   - Removes the DC component to isolate rapid signal changes.
   - Resistor: 4kΩ, Capacitor: 100nF.
2. **Amplification**:
   - Non-inverting operational amplifier (MCP6022).
   - Gain: 46, achieved with resistors (2kΩ and 90kΩ).
   - Adds a 1V DC offset for better signal processing.

### **Comparator**
- Converts analog signals into digital waveforms with thresholds determined by a voltage divider.
- Outputs square pulses representing binary levels.

---

## 🖥️ **Software Integration**
- Analyzes signal peaks and calculates frequency to distinguish species:
  - Abronia (571 Hz)
  - Dixonius (353 Hz).

---

## 📂 **Files**
- **Circuit Simulation**: `infrared_signal.asc` (LTSpice).
- **PCB Layout**: `infrared_signal_pcb.pdf`.
