# 🧪 Module Testing

This document outlines the software testing performed on the Radio, Ultrasound, Infrared, and Magnetic signal processing modules. Each module was rigorously tested to ensure accurate detection and processing of the respective signals.

---

## 📡 **Radio Signal Software**

### **Overview**
The software processes analog signals to determine their frequency. Using an Arduino, the system counts the number of rising edges over a defined period to calculate the frequency of the signal. The calculated frequencies are displayed on the serial monitor every 100 milliseconds to avoid excessive output clutter.

### **Algorithm Design**
The logic used for the radio signal frequency detection is illustrated in the following flowchart:
<img src="../../Images/Radio_flow_chart.png" alt="Radio Signal Flowchart" width="400" height="300"/>

### **Explanation**
1. **Frequency Calculation**:
   - The Arduino reads the analog signal and checks if the value crosses the defined threshold.
   - The frequency is determined by counting rising edges within an interval.
   - Every 1-second interval, the average frequency is calculated and displayed.

2. **Output**:
   - The frequency is output to the serial monitor every 100ms, allowing real-time monitoring.

### **Test Results**
The system successfully detected the frequencies of the radio signal during tests, as shown in the serial monitor output:
<img src="../../Images/Radio_code_Output.png" alt="Radio Signal Test Output" width="400" height="300"/>

---

## 🛰️ **Ultrasound Signal Software**

### **Overview**
The ultrasound module software decodes 4-character lizard names from digital signals received in UART format. The software handles bit-reversal, start/stop bits, and ensures stable output.

### **Explanation**
1. **Signal Decoding**:
   - Each character is received in reverse order (LSB first and MSB last).
   - Additional start (0) and stop (1) bits are handled by the program.

2. **Software Logic**:
   - The program detects the start bit (`0`) to begin reading the signal and uses the stop bit (`1`) to reset for the next character.
   - The decoding process ensures timing accuracy using `bitDuration` and properly saves characters in reverse order.

3. **Error Handling**:
   - The software checks the first character to ensure it begins with `#`, avoiding errors caused by looped signals.

### **Test Results**
During testing, the module successfully decoded various lizard names from ultrasound signals. An example output is shown below:
<img src="../../Images/Ultrasound_code_output.png" alt="Ultrasound Signal Test Output" width="400" height="300"/>

---

## 🌈 **Infrared Signal Software**

### **Overview**
This module processes infrared signals to calculate frequency and determine the lizard species. Instead of the previously implemented FFT algorithm, a simpler peak-counting method was used to minimize complexity and improve performance.

### **Algorithm Design**
The logic for infrared signal frequency detection is illustrated below:
<img src="../../Images/Infrared_flow_chart.png" alt="Infrared Signal Flowchart" width="400" height="300"/>

### **Explanation**
1. **Peak Detection**:
   - The software counts peaks to determine the time between them (period).
   - The frequency is calculated as the inverse of the period.

2. **Why Not FFT?**:
   - FFT was avoided due to storage issues and the need for an overly precise strategy.
   - The simpler algorithm is more resource-efficient and achieves the required accuracy.

### **Test Results**
The system correctly detected the frequencies for two predefined lizard species during tests:
- Abronia: **571 Hz**
- Dixonius: **353 Hz**

The test output is shown below:
<img src="../../Images/Infrared_code_Output.png" alt="Infrared Signal Test Output" width="400" height="300"/>

---

## 🧲 **Magnetic Signal Software**

### **Overview**
The magnetic signal module detects the magnetic polarity (North Pole, South Pole, or Neutral) to identify the lizard's orientation.

### **Explanation**
1. **Polarity Detection**:
   - The module compares the magnetic field readings from two sensors.
   - Differences in readings determine the polarity:
     - If the difference > 10: **North Pole**
     - If the difference < -10: **South Pole**
     - Otherwise: **Neutral**

2. **Integration**:
   - The software integrates seamlessly with the hardware to process magnetic signals in real-time.

### **Test Results**
Below is the serial monitor output showing accurate detection of magnetic polarities during testing:
<img src="../../Images/Magnet_code_output.png" alt="Magnetic Signal Test Output" width="400" height="300"/>

---

## 🔬 **Conclusion**

The software testing for all four modules—Radio, Ultrasound, Infrared, and Magnetic—was successful. Each module demonstrated accurate signal processing and reliable performance, meeting the design requirements. These results confirm the robustness of the hardware-software integration in the rover's signal detection and processing system.

---
