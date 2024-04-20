# Project Title
# Automatic Pump Control with Distance Monitoring using ESP32 and Blynk

1. Project Overview

This project automates a pump based on distance measured by an ultrasonic sensor connected to an ESP32 board. It displays the distance data in real-time on both the Blynk app and web dashboard (Blynk Cloud).

2. Features

Measures distance using an ultrasonic sensor.
Controls a pump based on the measured distance (configurable threshold).
Displays real-time distance data on the Blynk app and web dashboard.

3. Hardware Requirements

ESP32 development board (any model should work)
Ultrasonic sensor (e.g., HC-SR04)
Breadboard and jumper wires for connections
Pump (relay module required for connection)
LED (optional) for visual feedback

4. Software Requirements

Arduino IDE with ESP32 board support
Blynk library: https://github.com/blynkkk/blynk-library
Blynk app for your mobile device (available on iOS and Android)

5. Connections

Connect the ultrasonic sensor:
VCC to ESP32 5V
Trig to GPIO (Define pin number in code)
Echo to GPIO (Define pin number in code)
GND to ESP32 GND
Connect the pump to a relay module controlled by an ESP32 GPIO pin (Define pin number in code).
Connect the optional LED (with resistor) to another ESP32 GPIO pin (Define pin number in code).

6. Installation

Install the Blynk library in the Arduino IDE: Sketch -> Include Library -> Manage Libraries -> Search for "Blynk" and install.
Open the code in the Arduino IDE.

7. Configuration

Replace ssid and pass with your Wi-Fi credentials.
Replace BLYNK_AUTH_TOKEN with your Blynk authentication token from the app.
Define the GPIO pin numbers for the ultrasonic sensor (Trig, Echo), pump relay, and LED (if used) in the code.
Set the distance threshold for pump activation in the code.

8. Uploading and Running

Upload the code to your ESP32 board.
Open the Blynk app and create a new project.
Add widgets to visualize the distance data (e.g., Value Display) and control the pump (e.g., Switch).
Run the project in the app.

9. Blynk Cloud

In the Blynk app, navigate to Settings and link your project to Blynk Cloud.
Access the Blynk Cloud web dashboard ([invalid URL removed]) using your Blynk login credentials.
Your project should be displayed on the dashboard, allowing remote monitoring and control.

10. Functionality

The code continuously measures distance using the ultrasonic sensor.
It activates the pump if the distance falls below the defined threshold.
The distance data is sent to the Blynk app and web dashboard for real-time visualization.