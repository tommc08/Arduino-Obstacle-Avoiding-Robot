# Arduino-Obstacle-Avoiding-Robot
An Arduino-based autonomous robot that detects and avoids obstacles using an ultrasonic sensor, L298N motor driver, and servo motor. It scans its environment, reverses or turns when needed, and continues moving forward. A beginner-friendly mechatronics project with code and build documentation.
**📍 Project Goal:**

To build a self-driving robot using an ultrasonic sensor to detect obstacles and avoid collisions by autonomously reversing and turning. This project was designed to teach core concepts in mechatronics, embedded systems, and robotic control logic.

**📦 Equipment & Tools Used:**

| **Category** | **Items** |
| --- | --- |
| Microcontroller | Elegoo Uno R3 (Arduino compatible) |
| Motors | 2 x DC Gear Motors |
| Motor Driver | L298N Dual H-Bridge Motor Driver |
| Sensor | HC-SR04 Ultrasonic Distance Sensor |
| Servo | SG90 Micro Servo (to rotate the sensor for scanning) |
| Chassis | 2-wheel acrylic chassis with caster wheel |
| Power Supply | 4x AA battery pack with switch |
| Other | Breadboard, jumper wires, resistors, LEDs, sensor shield  |
| Tools | Tabiger Soldering Kit, AstroAI Multimeter, iFixit Toolkit |

**🛠️ Full Step-by-Step Build Log: Obstacle Avoiding Robot**

**🔹**

**Step 1: Planning & Goal Setting**

- Decided on first project: Obstacle Avoiding Robot
- Chose it because it teaches key mechatronics skills: motors, sensors, logic, power
- Reviewed the required hardware and tools

**🔹**

**Step 2: Tool & Kit Setup**

Collected and confirmed availability of:

- ✅ Elegoo UNO Super Starter Kit (Arduino-compatible)
- ✅ HC-SR04 ultrasonic sensor
- ✅ L298N motor driver
- ✅ 2 x DC motors
- ✅ SG90 Servo motor
- ✅ Soldering Kit (Tabiger)
- ✅ Multimeter (AstroAI)
- ✅ Electronics Toolkit (iFixit)

**🔹**

**Step 3: Learning the Basics**

- Learned about Arduino boards, digital/analog pins, breadboards
- Understood basic electronics concepts: voltage, current, ground, power rails
- Practiced wiring basic components on the breadboard
- Installed Arduino IDE on laptop
- Simulated components in Tinkercad Circuits
- Installed all components to chassis using double sided tape and super glue, screws and washers, bolts etc

**🔹**

**Step 4: Wiring the Components**

1. Connected:
    - HC-SR04 to A2 (Echo), A3 (Trig), 5V, GND
    - Servo to pin 11, 5V, GND
    - L298N to pins 2, 3, 4, 5 (motor control)
    - Motors to L298N output terminals
2. Wired the power system:
    - Battery pack (4x AA) → switch → L298N +12V
    - GND from battery → L298N GND
    - L298N 5V → Arduino 5V
    - GND → Arduino GND

**🔹**

**Step 5: Uploading and Testing Code**

- Wrote Arduino code using:
    - Servo.h to control ultrasonic scanning
    - NewPing.h to read distance values
- Created logic to:
    - Move forward by default
    - Reverse if object is ≤ 20 cm
    - Scan left/right and turn to clear the path
- Uploaded code and ran initial tests
- Used a simple test loop to verify motor movement and power delivery

**🔹**

**Step 6: Debugging Issues**

Identified and fixed key problems:

| **Issue** | **Solution** |
| --- | --- |
| Motors twitch but dont move | Power from USB was too weak, switched to battery pack |
| Motors stopped quickly | Improved solder joints to reduce resistance |
| Robot powered on, but nothing moved | Fixed wiring: connected 5V and GND from L298N to Arduino |
| Servo moved but robot didnt | Rewrote test loop to isolate power problem |
| Battery power didnt reach Arduino | Rerouted switch, 12V terminal properly |

**🔋 Power-On Test:**

- Flipped the switch → Arduino powered up
- Sensor servo rotated to scan surroundings
- Robot moved forward by default
- On detecting a nearby object (≤ 20 cm):
    - Reversed briefly
    - Turned either left or right based on which side was clearer
    - Continued forward after obstacle was avoided

**🧠 Skills & Concepts Learned:**

**🧩 Electronics:**

- Circuit wiring: connecting motors, sensors, servos, and drivers
- Breadboard prototyping and voltage flow understanding
- Power management: understanding current limits of USB vs battery
- Soldering techniques and their impact on performance

**🧠 Programming (C++/Arduino):**

- Writing and uploading code in Arduino IDE
- Using libraries like Servo.h and NewPing.h
- Controlling digital output pins for motors
- Using sensor data to influence behavior (if-else logic)
- Servo control for environmental scanning

**🤖 Robotics & Mechatronics:**

- Using an ultrasonic sensor to measure distance
- Making decisions based on sensor input (avoid obstacles)
- Driving motors forward/backward and turning using an H-bridge
- Creating an autonomous robot that can think and act without user control

**🔋 Debugging & Engineering Problem-Solving:**

- Diagnosing power issues (USB not enough current)
- Verifying connections using a multimeter
- Testing each module (motors, servo, sensor) independently
- Iteratively fixing wiring, solder joints, and logic errors


**🧩 Challenges Faced & Solutions:**

| **Problem** | **Solution** |
| --- | --- |
| Robot only moved for a second | Discovered USB couldnt power motors, switched to batteries |
| Robot didn’t move at all | Rewired power delivery: battery, switch,motor driver, Arduino |
| Unstable soldering | Re-soldered connections to motor terminals with more precision |
| Confusing pin mapping | Studied and matched code pin numbers to hardware correctly |
| Wheels not turning smoothly | Confirmed motor power and rewrote test loop for verification |

Another main problem was just with the motor I ordered was faulty and would need help to get started. Was because of low quality plastic..


**Summary** 

This project marks the successful completion of my first fully autonomous robot: an obstacle-avoiding vehicle built using Arduino, an ultrasonic sensor, and motor control logic. Through this build, I gained hands-on experience in electronics, coding, sensor integration, power management, and real-world troubleshooting. The robot can detect objects in its path, make decisions, and navigate independently. This foundation sets the stage for more advanced mechatronics and robotics projects as I continue developing my engineering skills.