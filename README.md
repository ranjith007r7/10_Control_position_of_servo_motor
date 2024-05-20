# 10_Control_position_of_servo_motor

# Servo Motor Position Control with Keypad

## Overview

This project enables the control of a servo motor's position using a 4x4 keypad connected to an Arduino. Each key on the keypad corresponds to a specific angle position of the servo motor. When a key is pressed, the servo motor moves to the corresponding angle position.

## Components

- Arduino board (e.g., Uno, Mega)
- Servo motor
- 4x4 Keypad
- Jumper wires

## Circuit Diagram

1. **Servo Motor**
   - Connect the signal wire of the servo motor to digital pin 10 on the Arduino.
   - Connect the power wire of the servo motor to 5V on the Arduino.
   - Connect the ground wire of the servo motor to GND on the Arduino.

2. **Keypad**
   - Connect the row pins of the keypad to digital pins 2, 3, 4, and 5 on the Arduino.
   - Connect the column pins of the keypad to digital pins 6, 7, 8, and 9 on the Arduino.

## Code Explanation

### Libraries

- `Servo.h`: For controlling the servo motor.
- `Keypad.h`: For interfacing with the keypad.

### Variables and Objects

- `servo`: Servo object for controlling the servo motor.
- `position`: Variable to store the current position of the servo motor.
- `keys[][]`: Array to define the layout of the keypad.
- `rowPins[]` and `colPins[]`: Arrays to define the pins connected to the rows and columns of the keypad.
- `kpd`: Keypad object for reading key presses.

### Setup

- Serial communication is initialized at 9600 baud.
- The servo motor is attached to pin 10.

### Loop

- The code continuously checks for key presses on the keypad.
- When a key is pressed, the corresponding angle position for the servo motor is determined based on the key pressed (1 for 0 degrees, 2 for 90 degrees, 3 for 180 degrees).
- The servo motor moves to the specified position.

## Usage Instructions

1. Assemble the circuit as per the circuit diagram.
2. Upload the provided code to the Arduino board.
3. Open the Serial Monitor from the Arduino IDE (Tools -> Serial Monitor) to view status messages.
4. Use the keypad to enter the desired angle position for the servo motor.
5. Observe the servo motor moving to the specified angle position.

## Example Output

- Pressing '1' on the keypad will move the servo motor to 0 degrees.
- Pressing '2' on the keypad will move the servo motor to 90 degrees.
- Pressing '3' on the keypad will move the servo motor to 180 degrees.

This project provides a simple and interactive way to control the position of a servo motor using a keypad, making it suitable for various robotics and automation applications.

---

