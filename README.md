# BLACKHAWK
This repository contains the flight software and supporting systems developed by our high school rocketry team for competition use. Our project focuses on designing, building, and testing an actively controlled model rocket with advanced avionics and control systems.

The rocket integrates multiple subsystems, including custom-designed printed circuit boards (PCBs), thrust vector control (TVC), airbrake deployment, and real-time flight control algorithms. These systems work together to improve flight stability, trajectory accuracy, and overall performance during powered ascent and descent.

At the core of the software is a state machine that manages each phase of flight, from ignition to apogee and recovery. Control is achieved through PID loops that dynamically adjust the rocket’s orientation using the TVC system, while additional logic governs airbrake actuation to regulate altitude and velocity.

This project reflects a combination of mechanical design, embedded systems, and software engineering, developed collaboratively in preparation for competitive rocketry events.


# Thrust Vector Control (TVC) and PID Control System

The thrust vector control (TVC) system is responsible for stabilizing and steering the rocket during powered ascent by actively adjusting the direction of the motor’s thrust. This is achieved by gimbaling the motor mount using two servos, allowing the thrust vector to be redirected in both the pitch (x-axis) and yaw (y-axis) directions.

To control this system, the rocket uses two independent PID (Proportional–Integral–Derivative) control loops—one for each axis. These control loops continuously calculate the error between the rocket’s current orientation (measured by onboard sensors such as an IMU) and the desired orientation, then apply corrections in real time.

Each PID loop consists of three components:

Proportional (P): Applies a correction proportional to the current error. Larger deviations from the desired orientation result in stronger corrective movements.

Integral (I): Accounts for accumulated error over time, helping eliminate steady-state offset and ensuring the rocket maintains its intended trajectory.

Derivative (D): Responds to the rate of change of the error, providing damping and reducing overshoot by anticipating future error trends.

By combining these three components, each PID loop produces a control signal that drives a servo motor. Together, the two servos adjust the motor mount angle, enabling precise, independent control of the rocket’s orientation in both axes.

This closed-loop control system allows the rocket to maintain stability, correct disturbances, and follow a controlled flight path throughout ascent. mount.
