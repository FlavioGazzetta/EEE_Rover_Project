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

**Oscilloscope Output Waveform**  
   <img src="../../Images/Radio_Output_waveform_from_Oscilloscope.png" alt="Radio Oscilloscope Output Waveform" width="400"/>

---

## 📊 **Test Results**
- Successfully identified species-specific signals and achieved accurate detection in controlled tests.

---

## 🖼️ **Circuits**
Below are the images of the circuits for the Radio Signal Processing module:

1. **Band-pass Filter Circuit**  
   <img src="../../Images/Radio_Band_pass_Filter_Circuit.png" alt="Radio Band-pass Filter Circuit" width="400"/>

2. **Non-Inverting Amplifier Circuit**  
   <img src="../../Images/Radio_non_inverting_amplifier_Circuit.png" alt="Radio Non-Inverting Amplifier Circuit" width="400"/>

3. **Envelope Detector Circuit**  
   <img src="../../Images/Radio_envelope_detector_circuit.png" alt="Radio Envelope Detector Circuit" width="400"/>

4. **Comparator Circuit**  
   <img src="../../Images/Radio_Comparator_circuit.png" alt="Radio Comparator Circuit" width="400"/>

5. **Full Circuit**  
   <img src="../../Images/Radio_Full_circuit.png" alt="Radio Full Circuit" width="400"/>

6. **PCB Full Circuit**  
   <img src="../../Images/Radio_PCB_Circuit.png" alt="Radio PCB Circuit" width="400"/>
