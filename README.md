🔥 Arduino Automatic Fire Fighting System

An Arduino-based automatic fire-fighting system that detects the direction of a flame using three flame sensors and automatically turns a water pump ON while positioning a servo motor toward the detected fire.

📌 Project Overview

This project is designed to demonstrate a simple automatic fire detection and extinguishing system using Arduino.

The system uses three flame sensors to detect fire from the left, center, and right directions. Based on the detected direction, a servo motor changes its position toward the fire, while a relay activates a water pump to extinguish it.

🚀 Features

- 🔥 Detects flame from three directions
- ↔️ Identifies whether the fire is on the left, center, or right
- ⚙️ Automatically positions the servo toward the detected fire
- 💧 Automatically switches the water pump ON when fire is detected
- 🛑 Turns the pump OFF when no fire is detected
- 📟 Displays sensor readings through the Serial Monitor
- 🤖 Fully automatic operation

🧰 Components Required
Arduino Uno
Flame Sensor Module
Servo Motor
Relay Module
Water Pump
Water Pipe/Nozzle
Jumper Wires
External Power Supply

«⚠️ If the servo or pump requires significant current, use a suitable external power supply. Make sure the Arduino and external supply have a common GND where required.»

⚙️ Working Principle

1. The three flame sensors continuously monitor the surroundings.
2. When the left sensor detects fire:
   - Servo moves to approximately 40°
   - Relay turns ON
   - Water pump starts spraying water
3. When the center sensor detects fire:
   - Servo moves to 90°
   - Relay turns ON
   - Water pump starts
4. When the right sensor detects fire:
   - Servo moves to approximately 140°
   - Relay turns ON
   - Water pump starts
5. When no fire is detected:
   - Pump turns OFF
   - Servo returns to 90°

💻 Software

The project is programmed using:

- Arduino IDE
- C/C++
- Arduino "Servo.h" library

Library Required

#include <Servo.h>

The "Servo" library is used to control the direction of the servo motor.

🧠 Control Logic

             Flame Sensors
          ┌──────┬──────┬──────┐
          │ Left │Center│Right │
          └──┬───┴───┬──┴───┬─┘
             │       │       │
             └───────┼───────┘
                     ↓
                 Arduino Uno
                 ↙        ↘
              Servo       Relay
                ↓           ↓
         Aim at Fire     Water Pump

📊 Sensor Logic

The program assumes that the flame sensor outputs:

LOW  → Fire detected
HIGH → No fire

If your flame sensor works with the opposite logic, the conditions in the Arduino code need to be reversed.

🎯 Applications

- Educational fire detection projects
- Arduino and embedded-system demonstrations
- Robotics projects
- Automatic fire-response prototypes
- Engineering college mini-projects

🔮 Future Improvements

The project can be further improved by adding:

- 🌡️ Temperature sensor
- 📱 Mobile notification system
- 📷 ESP32-CAM for visual monitoring
- 🚨 Buzzer alarm
- 📺 LCD/OLED display
- 🔋 Battery backup
- 🤖 Automatic robot movement toward the fire
- 💧 Water-level monitoring
- 📡 IoT-based remote monitoring
