# 🚁 Adaptive Control for an Aeropendulum

This repository contains the implementation of advanced adaptive and predictive control strategies applied to a physical Aeropendulum system. The project focuses on real-time system identification and the application of various control architectures using a microcontroller (Arduino).



## 🎯 Project Overview

An aeropendulum is a highly non-linear, underactuated system typically consisting of a pendulum arm with a motor-driven propeller at its end. Controlling its angle requires robust algorithms that can adapt to unmodeled dynamics and external disturbances. 

This project implements and compares different advanced control laws, relying on real-time parameter estimation.

## 🧠 Implemented Control Strategies

* **ELS (Extended Least Squares):** Used for online/offline system identification. It estimates the mathematical model of the aeropendulum's dynamics in real-time, handling colored noise better than standard RLS.
* **STR (Self-Tuning Regulator):** An adaptive control scheme that constantly updates the controller parameters based on the ELS estimations to maintain optimal performance despite changes in plant dynamics.
* **MPC (Model Predictive Control):** An advanced control strategy that optimizes a cost function over a receding prediction horizon to calculate the optimal control action, handling system constraints naturally.
* **IMC (Internal Model Control):** A control architecture that explicitly uses the plant model to design the controller, providing excellent robustness and setpoint tracking.

## 📂 Repository Structure

* `/aeropendulum` - Core plant models and baseline files.
* `/ELS.ino` & `/ELS` - Arduino implementation and data for the Extended Least Squares identification algorithm.
* `/Aeropendulo_STR`, `/Aeropendulo_STR_S0` - Source code and simulations for the Self-Tuning Regulator.
* `/aeropendulo_MPC`, `/aeropendulo_MPC_D2` - Implementations of the Model Predictive Controller (including variants).
* `/aeropendulo_IMC` - Internal Model Control implementation.
* `/mediciones` - Datasets containing the physical measurements and telemetry gathered from the hardware for offline analysis and validation.
* `/simulacion1` - Initial simulations to validate the control laws before hardware deployment.

## 🛠️ Hardware & Software Stack
* **Hardware:** Arduino (Microcontroller), DC Motor/Propeller, Rotary Encoder (for angle measurement).
* **Control Theory:** Adaptive Control, Predictive Control, System Identification.
* **Languages:** C++ (Arduino), MATLAB/Python (for offline data analysis and simulation).

## Results!!! (Indirect Adaptive STR)
![resize1-ezgif com-optimize](https://github.com/user-attachments/assets/d13bdbd1-de21-4533-9176-748621ea6824)

