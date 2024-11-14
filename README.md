# PID-LFR
PID Controled Line follower Roboto using 5CH sensor array and nano &amp; L298n Motor driver
For this line-following robot code, here is a circuit diagram and connection instructions to help you set up the components with an Arduino and an L298N motor driver. This robot will use five sensors for line detection, a push button to start the robot, and an LED for signaling.

### Components Needed:
1. **Arduino Uno** (or compatible microcontroller)
2. **L298N Motor Driver Module** (for controlling two DC motors)
3. **DC Motors** - 2
4. **5 Infrared (IR) Sensors** or **5 Line Sensor Modules** (for detecting the line)
5. **Push Button** (for starting the line-following sequence)
6. **LED** (for signaling the button press and other states)
7. **Battery Pack** (appropriate for powering motors and Arduino)
8. **Jumper Wires**

### Circuit Connections:
1. **Motor Connections**:
   - Connect **DC Motor A** to the **OUT1** and **OUT2** terminals of the L298N motor driver.
   - Connect **DC Motor B** to the **OUT3** and **OUT4** terminals of the L298N motor driver.
   - Connect **IN1** on the motor driver to Arduino **pin 6**.
   - Connect **IN2** on the motor driver to Arduino **pin 5**.
   - Connect **IN3** on the motor driver to Arduino **pin 4**.
   - Connect **IN4** on the motor driver to Arduino **pin 2**.
   - Connect **enA** on the motor driver to Arduino **pin 9** (for PWM control of Motor A).
   - Connect **enB** on the motor driver to Arduino **pin 3** (for PWM control of Motor B).

2. **IR Sensors**:
   - Connect each IR sensor to a separate analog pin on the Arduino:
     - Sensor 1 to **A0**
     - Sensor 2 to **A1**
     - Sensor 3 to **A2**
     - Sensor 4 to **A6**
     - Sensor 5 to **A7**
   - Connect the **VCC** of each sensor to **5V** on the Arduino.
   - Connect the **GND** of each sensor to the **GND** on the Arduino.

3. **Push Button**:
   - Connect one side of the push button to **Arduino pin 12**.
   - Connect the other side to **GND**.
   - The **INPUT_PULLUP** configuration in the code means no additional pull-up resistor is needed.

4. **LED**:
   - Connect the **positive leg** of the LED to **Arduino pin 13**.
   - Connect the **negative leg** of the LED to **GND** (you may add a 220-ohm resistor in series with the LED to limit current).

5. **Power Supply**:
   - Connect the **Arduino’s 5V and GND** pins to the VCC and GND of the sensors, LED, and button.
   - Power the **L298N motor driver** with an external battery pack via the 12V input terminal. 
   - **Connect the GND of the motor driver to the GND of the Arduino** to ensure a common ground.

After completing these connections, you should be able to upload the code to the Arduino and use the push button to start the line-following operation.
