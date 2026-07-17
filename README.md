# Self-Balancing Robot — from scratch

A two-wheeled self-balancing robot built end-to-end, using an advanced (cascaded) PID
control policy. The robot estimates its body angle and continuously adjusts motor
output to maintain balance, forming a closed-loop control system similar to the basic
principle behind Segway-like robots.

The project combines hardware integration, sensor feedback, real-time control, and
parameter tuning. Its broader significance lies in demonstrating how classical control
methods can stabilize unstable physical systems, providing a foundation for more
advanced robotics control topics such as state feedback, trajectory tracking, and
model-based control.

## Highlights

- Engineered a self-balancing robot by integrating an **Arduino Nano**, **MPU6050 IMU**,
  **HC08 motor driver**, encoder-equipped DC motors, and power regulation circuitry into
  a real-time embedded control platform.
- Designed a **dual-loop (cascaded) PID controller** that regulates the robot's pitch
  angle through nested angle and velocity feedback, eliminating long-term drift observed
  with single-loop balancing and improving recovery robustness.
- Implemented **interrupt-driven encoder processing** with both fixed-time and
  fixed-pulse velocity estimation, evaluating their responsiveness and noise
  characteristics to achieve reliable motor feedback for real-time control.

## Hardware

| Part | Role |
| --- | --- |
| Arduino Nano | Main controller |
| MPU6050 | 6-axis IMU (pitch angle) |
| HC08 | Motor driver |
| DC motors + encoders | Actuation + speed feedback |
| Buck converter / 3S LiPo | Power regulation |

## Demo

Open [`index.html`](index.html) in a browser to view the project overview image and the
demo video.

- `self_balancing_robot.png` — system overview (architecture, wiring, control, results)
- `self_balancing_car.mp4` — live balancing demo
