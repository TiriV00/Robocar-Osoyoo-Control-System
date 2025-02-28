# Osoyoo Model 3 Control System

## Introduction
This project was developed as part of a university exam. The goal was to create a **Control System** for the toy car **Osoyoo Model 3** (https://osoyoo.com/it/2020/05/22/osoyoo-model-3-v2-0-robot-learning-kit/), enabling it to perform custom functions. The car was equipped with an **STM32F411RE** microcontroller.

**Note**: The car originally comes with an **Arduino Uno** microcontroller, but we decided to replace it with the **STM32F411RE** to allow the loading of **Simulink** models.

## Requirements
To run the provided code, the following software is required:  
- **MATLAB** and **Simulink**  
- **STM32CubeIDE**, the official IDE for STM microcontrollers  

**Before working with these files, we highly recommend reading the report** `Control_System_Tiri-Rovighi_Report`, which provides a complete explanation of the project.

## Repository Structure
This repository contains:  
- **`Control_System_Tiri-Rovighi_Report`**: A detailed document explaining the entire project.  
- **`videos` folder**: Contains videos showcasing the toy car performing the described functions.  
- **`Scripts` folder**: Contains the `.m` and `.slx` files necessary to run the project on MATLAB and Simulink.  

## Workflow
To successfully run the simulations, follow these steps:  
1. Connect the car to your PC via USB.  
2. Use **STM32CubeIDE** to generate a **C++ file** for mapping the microcontroller's pins.  
3. Run the `model_main_v10.slx` file in **Simulink** with the option **Build, Deploy and Start**.  

## Disputes
Once the work was submitted for evaluation, the main criticism was our **inability to use the microcontroller's onboard timers**.  

Since we didn't use them, we had to create our own counters to trigger functionalities, which turned out to be **inefficient and difficult to manage**.  
Using the **onboard timers** would have provided significant advantages in terms of **timing control, functionality management, and ease of tuning/programming**.  

We **highly encourage** you to replace our custom counters with the **microcontroller's internal timers** if you can.  

## Authors
- [Federico Rovighi](https://github.com/federovighi) - MUNER, EEIV - ADE Master's Degree  
- [Valerio Tiri](https://github.com/TiriV00) - MUNER, EEIV - ADE Master's Degree  
