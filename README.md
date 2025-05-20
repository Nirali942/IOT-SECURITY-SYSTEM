TASK-3
# IOT-SECURITY-SYSTEM

🔐 IoT Security System: Motion Detection + Image Capture + Mobile Alert

✅ Project Objective
To build a functional IoT security system prototype that:

Detects motion using a PIR sensor,

Captures an image using a camera module,

Sends an instant alert (with image) to the user's mobile app.

🛠️ Required Components
Hardware
ESP32-CAM module (with built-in Wi-Fi and camera)

PIR Motion Sensor (HC-SR501)

5V Power Supply or USB programmer

Jumper wires

Optional: Breadboard, Relay module (for alarm/light), MicroSD card (to store images)

 💻 Software Requirements

- [Arduino IDE](https://www.arduino.cc/en/software)
- ESP32 board package installed in Arduino IDE
- Blynk library (install via Library Manager)
- Blynk IoT App (Android/iOS)
- Internet Wi-Fi connection

⚙️ System Workflow
Motion Detection: PIR sensor detects movement.

Image Capture: ESP32-CAM captures an image when motion is detected.

Alert Sent: An alert (with captured image or notification) is sent to the user’s mobile app using Blynk or Telegram.

Optional: Activate a buzzer or light using relay.

🔌 Circuit Connection
ESP32-CAM Pin 	PIR Sensor
3.3V             VCC
GND	             GND
GPIO13	         OUT

Use an FTDI programmer to upload code to ESP32-CAM.

Connect:

U0R → TX of FTDI

U0T → RX of FTDI

IO0 → GND (only during upload)

🔧 Arduino IDE Setup

1. Install ESP32 board URL:
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json

📲 Blynk Setup
Create a new project in Blynk.

Choose device: ESP32

Add a Notification widget and enable event notification

Use event named motion_alert in the code.

📲 Blynk Setup (Mobile)

1. Download **Blynk IoT app**.
2. Create a new project:
- Device: ESP32
- Connection: WiFi
3. Add a **Notification** widget.
4. Enable "Notify when hardware goes offline".
5. Copy the **Auth Token** to use in the code.
6. In the web dashboard, create an **Event** named 'motion_alert'.

  🔑 Configuration

In the Arduino code, replace the placeholders with your details:

const char* ssid = "YOUR_WIFI_SSID";
const char* password = "YOUR_WIFI_PASSWORD";
char auth[] = "YOUR_BLYNK_AUTH_TOKEN";

📦 Deliverables
✅ Fully working prototype with real-time alerts

📷 Motion detection + Image capture

📱 Mobile app (Blynk) receives alert

🔔 Optional: Buzzer/light activation

📖 README file with setup instructions (on request)
