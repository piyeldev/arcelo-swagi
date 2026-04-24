# 🔌 Wiring Diagram and Assembly

In this page, we will learn how are the parts wired together, and how to assemble them. 

Let's start with the overall view of how the robot is wired together.

### Overall
![wiring diagram](/img/wiring_diagram.png)

**some parts may not reflect the real ones. This is for illustration purposes only.*

It is all centered to the ESP32. The ESP32 is the one facilitating communication between the phone through WiFi, and sending commands to the arduino and its motor drive shield, and the F5305S Power MOSFETs.

You can see that its pretty messy. But it will all make sense once we tackle it in groups of parts. 

Let's start with the Arduino Uno, its L293D motor driver shield.

### Arduino Uno and L293D Motor Driver Shield
<img src="/img/arduino-and-driver.png" alt="Arduino and Motor Driver Shield and Parts" width="500" /> 

Starting with the arduino, you can immediately notice that you can't see the arduino itself in this image. This is because a motor driver shield is attached to it. Moving on to the motor driver shield's screw terminals (the green ones, that has 5 terminals each), you can see that it is divided into 4 pairs: M1, M2, M3, M4 (except for the ones in the center). Each pair can drive DC motors, and 2 pairs can drive 1 stepper motor. 

To connect a dc motor to a terminal, solder a wire into the dc motors terminals, and connect it to the shield's terminals. The <a>polarity</a> is not important, as long as all motors have the same positioning of wires, and that the FORWARD command in the code (we will get into later) correctly moves the motors forward. 

To connect a servo motor, use the SERVO terminals (bottom left corner). Make sure to identify the wires correctly as wrong connection can damage the servo motor. 

For more information about the L293d Motor driver and how to use it, you may refer to <a href="https://lastminuteengineers.com/l293d-motor-driver-shield-arduino-tutorial/" target="_blank">this guide</a>.


### ESP32 and Arduino
<img src="/img/esp_and_arduino.png" alt="ESP and Arduino" width="500" /> 

Before we 
<img src="/img/esp32_pinout.png" alt="ESP32 C3 SuperMini Pinout" width="500" /> 
 