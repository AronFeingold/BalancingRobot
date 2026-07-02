# BalancingRobot

A self-balancing robot built entirely from scratch — hardware and software.

## Demo
[Watch it balance](https://youtube.com/shorts/VkTLqgiC5PM)

## How it works
The robot uses a **PID control loop** to stay upright:
1. The **MPU6050 IMU** continuously measures the robot's tilt angle
2. The **Arduino Nano** reads this angle and calculates how far from vertical the robot is
3. The **stepper motors** adjust speed and direction to catch the robot before it falls
4. The PID values required significant fine-tuning — too aggressive and the robot overcorrects and falls the other way; too gentle and it can't react fast enough

## Components
| Part | Description |
|------|-------------|
| Arduino Nano | Microcontroller / brain |
| MPU6050 | Inertial measurement unit (IMU) for angle sensing |
| Stepper Motors (x2) | Drive wheels |
| Motor Drivers (x2) | Control stepper motors from Arduino |
| Custom frame | Built from scratch |

## What I learned
- PID control theory and real-world tuning
- Working with IMU sensors over I2C
- Stepper motor control
- The importance of mechanical precision — even small frame imbalances affect stability

## Built with
- C++ / Arduino IDE
