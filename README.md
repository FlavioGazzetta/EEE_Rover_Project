# 🛸 EEE Rover Project

**Group 29 - Electronics Design Project**

<img src="./Images/rover_front.png" alt="Rover Image" width="400"/>

---

### 🌟 **Overview**
The **EEE Rover Project** is a collaborative engineering initiative designed to develop a remote-controlled rover that can identify and analyze signals emitted by simulated lizards in an arena. The rover integrates advanced hardware and software to process multiple signal types and provides users with real-time data through a sleek web interface.

---

### 🚀 **Features**
- **Signal Detection & Processing**:
  - 🛰️ **Radio Signals**: Decodes modulated signals to identify lizard species.
  - 📡 **Ultrasound Signals**: Extracts digital data to display lizard names.
  - 🌈 **Infrared Signals**: Filters and analyzes peaks to identify frequencies for species recognition.
  - 🧲 **Magnetic Polarity**: Identifies the magnetic polarity to further distinguish species.

- **Remote-Control Functionality**:
  - Virtual joystick and user-friendly web interface for seamless rover operation.
  - Wi-Fi-based control with dynamic data updates.

- **Lightweight, Compact Design**:
  - 3D-printed chassis and custom PCBs ensure portability and agility.

---

### 🛠️ **System Components**
| Component                 | Functionality                       |
|---------------------------|-------------------------------------|
| **ESP32 Microcontroller** | Processes signals and handles control commands. |
| **Radio Receiver Circuit**| Decodes lizard species from modulated radio signals. |
| **Ultrasonic Transceiver**| Detects and demodulates 40kHz signals. |
| **Infrared Phototransistor**| Analyzes IR frequencies for species identification. |
| **Magnetic Sensors**      | Detects and processes magnetic polarities. |
| **Web Interface**         | Provides a virtual joystick for user control. |

---

### 🔍 **How It Works**
1. **Signal Processing**:
   - Signals from lizards are detected via sensors and processed through circuits to extract meaningful data.
   - Results (e.g., species name or frequency) are sent to the web interface.
   
2. **Rover Control**:
   - Use a virtual joystick to maneuver the rover (forward, backward, turn left/right).
   - Commands are processed via Wi-Fi and executed on the ESP32.

3. **Real-Time Data Visualization**:
   - Detected lizard species are displayed on the web interface for easy user interaction.

---

### 🔮 **Future Improvements**
- **Chassis Redesign**: Optimize for better weight distribution and stability.
- **Enhanced Signal Processing**: Improve stability and expand detection range.
- **Energy Efficiency**: Explore advanced motor control algorithms.
- **Sensor Upgrades**: Reduce environmental interference for more accurate readings.

---

### 🧑‍🤝‍🧑 **Team Members**
| Name             | Contribution                          |
|------------------|--------------------------------------|
| Flavio Gazzetta  | Integration & Infrared Signal Hardware Design|
| Michael Li       | Integration & Infrared Signal Analysis |
| Zecheng Zhu      | Ultrasound Signal Software & Reporting |
| Yufeng Wu        | Radio Signal & Magnetic Polarity     |
| Shenghong Liu    | Integration & Hardware Design        |

---

### 📚 **Documentation**
- [Hardware Design Details](./docs/hardware.md)
- [Software Implementation](./docs/software.md)
- [Project Report](./docs/project_report.pdf)

---

### 📂 **Repository Structure**
```plaintext
EEE_Rover_Project/
├── Hardware/
│   ├── PCB_Designs/
│   ├── 3D_Models/
├── Software/
│   ├── Arduino_Sketches/
│   ├── Web_Interface/
├── Images/
├── Docs/
│   ├── hardware.md
│   ├── software.md
│   ├── project_report.pdf
├── README.md
