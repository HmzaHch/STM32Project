# STM32 Embedded Firmware & Hardware Engineering Platform

[![Platform](https://img.shields.io/badge/Architecture-ARM%20Cortex--M-blue.svg?style=flat-square)](https://github.com/HmzaHch/STM32Project)
[![Language](https://img.shields.io/badge/Language-Embedded%20C-brightgreen.svg?style=flat-square)](https://github.com/HmzaHch/STM32Project)
[![IDE](https://img.shields.io/badge/IDE-Keil%20uVision%20%2F%20STM32CubeIDE-orange.svg?style=flat-square)](https://www.keil.arm.com/)
[![Config](https://img.shields.io/badge/Tools-STM32CubeMX-red.svg?style=flat-square)](https://www.st.com/)
[![Hardware](https://img.shields.io/badge/Hardware-STM32G4%20%2F%20STM32F1-purple.svg?style=flat-square)](https://github.com/HmzaHch/STM32Project)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)

A structured repository containing embedded firmware developments, register-level drivers, peripheral integrations (HAL/CMSIS), and hardware interface designs for STMicroelectronics ARM Cortex-M microcontrollers.

---

## 🌟 Repository Overview

This repository demonstrates bare-metal and HAL-based firmware engineering, hardware debugging, and real-time embedded systems principles:

- **Peripherals & Drivers:** GPIO control, Hardware Timers (TIM), Pulse Width Modulation (PWM), External Interrupts (EXTI), and Clock Configuration (RCC).
- **Communication Protocols:** Universal Asynchronous Receiver-Transmitter (UART/USART), I2C, Serial Peripheral Interface (SPI), and Controller Area Network (CAN Bus).
- **Toolchains & Workflows:** Configured for seamless development using **STM32CubeMX**, **Keil MDK-ARM (uVision)**, and **STM32CubeIDE**.
- **Hardware Targets:** ARM Cortex-M series (STM32F103, STM32G431) with debugging via ST-LINK V2/V3 and serial telemetry.

---

## 📁 Project Structure

```text
STM32Project/
├── EXEMPLELEDs/               # GPIO & Clock Management Module
│   ├── STM32CubeMX/           # Clock tree configuration & peripheral init files
│   ├── Listings/              # Compiler listings and map files
│   ├── Objects/               # Compiled binary/HEX artifacts
│   ├── RTE/                   # Keil Run-Time Environment components
│   └── BlinkLEDs.uvprojx      # Keil uVision project workspace
├── README.md                  # Project documentation
└── .gitignore                 # Filtered build outputs and user-specific IDE caches
```

---

## ⚙️ Development Environment & Toolchain

| Component | Specification |
| :--- | :--- |
| **Microcontroller Family** | STMicroelectronics STM32 (ARM 32-bit Cortex-M) |
| **Firmware Framework** | STM32Cube HAL / CMSIS Core |
| **Integrated Development Environment** | Keil uVision 5 (MDK-ARM) / STM32CubeIDE |
| **Code Configurator** | STM32CubeMX |
| **Hardware Debugger** | ST-LINK V2 / V3 (SWD interface) |

---

## 🚀 How to Build and Flash

### 1. Prerequisites
- Install [Keil MDK-ARM](https://www.keil.arm.com/) or [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html).
- Install the required STM32 Device Family Pack (DFP) for your microcontroller family.
- Connect your ST-LINK programmer via SWD (`SWDIO`, `SWCLK`, `GND`, `3V3`).

### 2. Opening the Project
1. Navigate to the project directory:
   ```bash
   cd STM32Project/EXEMPLELEDs
   ```
2. Double-click `BlinkLEDs.uvprojx` to open in Keil uVision.

### 3. Build & Download
- Press **F7** (or click *Project ➔ Build Target*) to compile the project.
- Press **F8** (or click *Flash ➔ Download*) to program the firmware onto the target MCU.
- Start a debugging session (**Ctrl + F5**) to step through code, inspect core registers, and monitor variable states in real-time.

---

## 🔬 Key Engineering Practices Implemented

1. **Deterministic Timing:** Configured hardware SysTick and General-Purpose Timers rather than blocking software delay loops.
2. **Modular Architecture:** Clear separation between hardware abstraction layers, peripheral initialization, and application logic.
3. **Low-Power Considerations:** Optimized clock trees (HSE/HSI and PLL scaling) to minimize power draw during standby or active execution.
4. **Resilient Hardware Interface:** Debounced inputs, current-limited outputs, and clean interrupt vectors.

---

## 👨‍💻 Author

**Hamza HACHOUM**  
*State Engineer in Applied Sciences and Technology (Embedded Systems & IoT)*  
*ISIMG, University of Gabès*  
- **LinkedIn:** [hamza-hachoum-186319227](https://www.linkedin.com/in/hamza-hachoum-186319227)  
- **GitHub:** [@HmzaHch](https://github.com/HmzaHch)  
- **Email:** hamza.hachoum@gmail.com
