# Inverse Kinematics Solver

## Overview

This project is an inverse kinematics (IK) solver that computes the joint angles required for a robotic arm or chain to reach a desired endpoint. The system utilizes a combination of forward kinematics, Jacobian matrix computation, and Newton's Method to iteratively solve for the optimal configuration of joints. Interactive visualizations demonstrate the process, allowing users to experiment with chain movements in real time.

---

## Key Features

### Core Functions

- **Forward Kinematics (****`chain`****)**: Computes the position of the endpoint based on given joint angles.
- **Jacobian Computation (****`dchain`****)**: Calculates the Jacobian matrix for the chain, which describes the relationship between joint angle changes and endpoint position changes.
- **Inverse Kinematics Solver (****`newton`****)**: Implements Newton's Method with a pseudoinverse of the Jacobian to iteratively minimize the error between the current and target positions.

### Interactive Demo

- **Visual Interface (****`ik_demo`****)**: Allows users to interact with a chain of joints through drag-and-drop mechanics. Users can set a target position and observe the chain adjust in real time to reach the target.
- **Scalability**: Demonstrates chains with different numbers of segments (e.g., 4 segments and 30 segments). Performance varies with chain complexity.

---

## How It Works

1. **Forward Kinematics:**

   - Input: Array of joint angles.
   - Output: Endpoint position computed through recursive summation of joint positions.

2. **Jacobian Matrix:**

   - Captures the partial derivatives of endpoint position with respect to joint angles.
   - Enables efficient computation of angle adjustments for IK solving.

3. **Newton's Method:**

   - Iteratively adjusts joint angles to minimize positional error.
   - Leverages the pseudoinverse of the Jacobian to compute optimal updates.

4. **Interactive Visualization:**

   - Users can drag the endpoint to set a target position.
   - The chain dynamically adjusts to follow the target.

---

## Environment Setup

To ensure proper execution of the code, use the provided `.yml` file in the repository to set up the required environment. This file includes all necessary dependencies and configurations for running the project smoothly.

---

## Acknowledgments

This project was developed as a part of the Dartmouth CS70 curriculum, Winter 2024.

---

## Enjoy!

Test it out with the provided live demos and observe the fascinating behavior of inverse kinematics in action.

---

## License

This project is distributed under the MIT License. Refer to the LICENSE file for detailed terms and conditions.

