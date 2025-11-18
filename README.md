This repository contains the complete embedded firmware for a real-time photoplethysmography (PPG) signal simulator, display, and heart rate monitor. The project is developed in C using the STM32 HAL libraries and runs on the STM32F429I-DISCOVERY board.

The application demonstrates a range of advanced embedded systems concepts, including bare-metal GUI development, real-time digital signal processing, and algorithm implementation on an ARM Cortex-M4 microcontroller.

<img width="530" height="713" alt="image" src="https://github.com/user-attachments/assets/0f7fa912-d94f-4a66-9df2-f228f64873d7" />

---

## Key Technical Features

*   **ARM Cortex-M4 Development:** Firmware developed entirely in C using the industry-standard **STM32 HAL library**, targeting a powerful STM32F429 microcontroller.
*   **Bare-Metal Graphical User Interface (GUI):** A full user interface was developed from scratch on the board's color LCD using the ST BSP library. The UI includes interactive touchscreen buttons for "Pause" and "Record," graph axes, and a live-plotting signal display.
*   **Real-Time Digital Signal Processing (DSP):** Implemented a real-time **IIR digital filter** directly on the microcontroller to process the PPG signal, removing DC offset and smoothing the waveform for analysis.
*   **Heart Rate Algorithm:** Developed a **peak detection algorithm** in C that analyzes the filtered waveform to identify individual heartbeats and calculate the beats-per-minute (BPM) in real-time.
*   **Interrupt-Driven Signal Generation:** Utilized a hardware timer interrupt (`HAL_TIM_PeriodElapsedCallback`) to generate a simulated PPG signal at a consistent 100Hz, ensuring the system operates in a deterministic, event-driven manner.

---

## Technologies & Tools

| Category                  | Technologies & Tools                                      |
| ------------------------- | --------------------------------------------------------- |
| **Microcontroller**         | STM32F429ZIT6U (ARM Cortex-M4)                            |
| **Development Board**       | STM32F429I-DISC1                                          |
| **Language**                | C                                                         |
| **Libraries & Frameworks**  | STM32 HAL Library, Board Support Package (BSP)            |
| **Core Concepts**           | Bare-Metal GUI, Real-Time DSP, Interrupts, Touchscreen Input, LTDC |
| **Development Environment** | STM32CubeIDE (or Keil/IAR)                                |
| **Version Control**       | Git                                                       |
