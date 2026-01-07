# IoT-Based-Remote-Heartbeat-Monitoring-System
📌 Project Overview
This project is an IoT-based prototype designed for Remote Patient Monitoring (RPM). The system enables real-time cardiac tracking, allowing health data to be transmitted from a wearable device to a cloud-based dashboard. This solution addresses "Smart City" healthcare challenges by reducing the need for physical hospital visits for routine monitoring.

**🛠 System Architecture & Flow**
As the System Architect, I designed the following 4-tier data pipeline:

Sensing Layer: A Pulse Sensor captures analog heart rate signals from the user.

Processing & Connectivity: An Arduino Uno handles the initial signal processing. The data is then passed to a NodeMCU (ESP8266), which provides the Wi-Fi bridge.

Cloud Integration: The processed BPM (Beats Per Minute) data is sent via the Firebase Arduino Client to a Firebase Realtime Database.

Visualization: A frontend dashboard (Mobile/Web) listens to Firebase updates to display live health metrics to physicians or caregivers.

**🚀 Key Technical Challenges Overcome**
Data Consistency: Ensuring the connection between the Arduino and NodeMCU remained stable during data transmission.

Latency: Optimizing the Firebase update frequency to ensure "real-time" monitoring without overwhelming the hardware memory.

Signal Noise: Researching logic to filter out "false beats" caused by minor sensor movement.

**💻 Technologies Used**
Hardware: Arduino Uno, NodeMCU ESP8266, Pulse Oximeter Sensor.

Software: C++ (Arduino IDE), JavaScript (for dashboard logic).

Cloud: Google Firebase.

**📈 Future Enhancements **
To scale this prototype for a full Smart City infrastructure, I planned the following future upgrades:

Encryption: Implementing SSL/TLS encryption for HIPAA-compliant data security.

Edge Computing: Processing data locally on the ESP8266 to trigger emergency alerts even if the Wi-Fi connection is lost.

GPS Integration: Adding a GPS module to locate patients instantly in case of a cardiac emergency in an urban environment.
