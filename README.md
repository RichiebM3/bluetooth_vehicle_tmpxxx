# bluetooth_vehicle_tmpxxx
Bluetooth controlled vehicle using a tmpxxx microcontroller.
# PWM Motor Driver Lab

## Overview
This project implements a PWM motor driver using a TM4C123GH6PM microcontroller. The system controls two DC motors using a dual H-bridge (L298N) and communicates with a Bluetooth module (HC-05) for remote control. The motors can move forward, backward, and turn at specified angles.

## Author
**Richard A Bruce**

## Components
- **Microcontroller:** TM4C123GH6PM
- **Motor Driver:** L298N Dual H-Bridge
- **Bluetooth Module:** HC-05
- **Programming Language:** C

## Features
- Control two DC motors with PWM signals.
- Bluetooth communication for remote control.
- LED indicators for motor status.
- Commands for moving forward, backward, stopping, and turning.

## Code Structure
The code is organized into several key functions:

- **Motor Control Functions:** Manage motor movements (forward, backward, stop, turns).
- **Bluetooth Functions:** Handle Bluetooth communication for receiving commands.
- **PWM Initialization:** Set up PWM for motor control.

### Key Functions
- `PWM_Init()`: Initializes PWM for motor control.
- `frontDrive()`: Moves the motors forward.
- `reverseDrive()`: Moves the motors backward.
- `stopMotors()`: Stops both motors.
- `Bluetooth_init()`: Initializes the Bluetooth module.
- `blueTooth_Read()`: Reads commands from the Bluetooth module.

## Setup Instructions
1. **Hardware Setup:**
   - Connect the L298N motor driver to the TM4C123GH6PM microcontroller.
   - Connect the HC-05 Bluetooth module to the appropriate UART pins.
   - Ensure the motors are connected to the L298N outputs.

2. **Software Setup:**
   - Make sure to have the appropriate development environment set up for programming the TM4C123GH6PM (e.g., Keil, Code Composer Studio).
   - Copy the provided code into your development environment.

3. **Compiling and Uploading:**
   - Compile the code and upload it to the microcontroller using the appropriate programmer.

## Usage Instructions
1. Power on the system.
2. Ensure the Bluetooth module is paired with your device.
3. Use a Bluetooth terminal app to send commands to the microcontroller.
   - **Commands:**
     - `S`: Move forward
     - `B`: Move backward
     - `H`: Stop
     - `C`: Turn left 45 degrees
     - `D`: Turn right 45 degrees
     - `E`: Turn left 90 degrees
     - `F`: Turn right 90 degrees

4. Observe the LED indicators for the current motor status:
   - **Red LED**: Motors stopped
   - **Green LED**: Moving backward
   - **Blue LED**: Moving forward

## Error Handling
- The system includes checks for Bluetooth communication errors and provides feedback via the serial output.

## Conclusion
This PWM motor driver project demonstrates how to control DC motors using PWM signals and Bluetooth communication. It serves as an excellent introduction to embedded systems, motor control, and wireless communication.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

