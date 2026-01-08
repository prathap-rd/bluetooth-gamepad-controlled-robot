# Bluetooth Gamepad Controlled Robot (HC-05 + L298N)

## Problem Statement
Design a two-wheel robot that can be controlled wirelessly using a Bluetooth gamepad via an HC-05 module.

## Components Used
- Arduino Uno
- L298N Motor Driver
- DC Motors (2)
- HC-05 Bluetooth Module
- External Power Supply
- Connecting Wires

## Pin Configuration

### L298N ↔ Arduino
| L298N Pin | Arduino Pin | Function |
|----------|-------------|----------|
| IN1 | 9  | Motor A direction |
| IN2 | 10 | Motor A direction |
| IN3 | 11 | Motor B direction |
| IN4 | 12 | Motor B direction |

### HC-05 ↔ Arduino
| HC-05 Pin | Arduino Pin | Function |
|----------|-------------|----------|
| TX | 2 | Bluetooth RX |
| RX | 3 | Bluetooth TX (via resistor divider) |

## Control Commands
| Command | Action |
|--------|--------|
| F | Forward |
| B | Backward |
| L | Left |
| R | Right |
| X | Stop |
| A | Start / Resume |
| P | Pause |

## Circuit Diagram
![Circuit Diagram]()

## Working Explanation
The Arduino receives control commands from a Bluetooth gamepad through the HC-05 module. Based on the received command, motor direction pins of the L298N driver are controlled to move the robot forward, backward, left, right, or stop.

## How to Run
1. Upload the code to Arduino Uno
2. Pair HC-05 with the mobile gamepad app
3. Open the app and send control commands
4. Observe robot movement
