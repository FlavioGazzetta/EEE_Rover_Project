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

## 📊 **Test Results**
- Successfully identified frequencies of 571Hz (Abronia) and 353Hz (Dixonius).

---

## 🖼️ **Circuits**
Below are the images of the circuits for the Infrared Signal Processing module:

1. **Infrared Circuit**  
   <img src="../../Images/Infrared_circuit.png" alt="Infrared Circuit" width="400"/>

2. **Oscilloscope Output Waveform**  
   <img src="../../Images/Infrared_ouput_waveforms_from_Oscilloscope.png" alt="Infrared Output Waveform" width="400"/>

3. **Infrared Processing Pipeline**  
   <img src="../../Images/Infrared_pipeline.png" alt="Infrared Pipeline Diagram" width="400"/>
