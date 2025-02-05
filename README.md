# Ball and Beam Control System
This project implements a Ball and Beam control system using an ESP32 microcontroller, an HC-SR04 ultrasonic sensor, an MG996R servo motor, LEDs, a volume potentiometer, and a 5V 2.5A adapter. The goal of this project is to provide a testbed for studying dynamic control concepts and implementing PID control algorithms in nonlinear systems.

## Features
- PID Control: Implements a PID algorithm to adjust the beam angle and maintain the ball's balance.
- Median Filtering: Uses a median filter to reduce noise from the HC-SR04 sensor's distance readings.
- Stability Detection: Monitors system stability by comparing the measured distance to the setpoint, with an LED indicator when the ball is at the setpoint.
- Stuck Detection: Detects when the ball is stuck (i.e., when no significant movement is detected) and applies a jolt to free it.
- Setpoint Adjustment: Allows the user to adjust the setpoint using a volume potentiometer with exponential smoothing.
- LED Status Indicators: Utilizes green and red LEDs to indicate power presence and when the ball reaches the setpoint.
## Hardware Components
- ESP32: The central processor for data processing and executing control algorithms.
- HC-SR04 Ultrasonic Sensor: Measures the distance of the ball from a reference point.
- MG996R Servo Motor: Adjusts the beam angle to control the ball’s movement.
- LEDs: Indicate the system status (e.g., power supply active and ball reaching setpoint).
- Volume Potentiometer (10KΩ): Allows the user to adjust the setpoint.
- Ball and Beam Structure: A 45 cm beam with an effective ball movement range from 3 cm to 37 cm.
- 5V 2.5A Adapter: Provides the required power to all components.
## How to Use
  ### Hardware Setup:
  - Connect the HC-SR04 sensor’s trig and echo pins, the servo motor, the volume potentiometer, the LED, and the adapter to the ESP32 using the following pin configuration:
  - Trig: Pin 12
  - Echo: Pin 14
  - Servo: Pin 27
  - Potentiometer: Pin 34
  - LED: Pin 13
  - Ensure that your power supply (5V 2.5A) is correctly connected to provide stable power.
  ### Uploading the Code:
  - Open the main.ino file in the Arduino IDE or PlatformIO.
  - Upload the code to your ESP32.
  ### Monitoring and Testing:
  - Use the Serial Monitor (set to 115200 baud) to view sensor readings, system status (stability and stuck detection), and servo commands.
  - Adjust the potentiometer to change the setpoint and observe the PID control action.
![photo_2025-02-05_10-41-52](https://github.com/user-attachments/assets/eefa5a34-93ce-4fb8-8270-451abd8edcac)
![image_2025-01-31_06-47-55](https://github.com/user-attachments/assets/96f6db8f-9723-4892-8a4e-bf7f00c2569d)
![photo_2025-02-05_10-48-12](https://github.com/user-attachments/assets/222691ff-7aaf-4fe6-b66a-9b0f3237405f)
