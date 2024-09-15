# Embedded C - STM32

Aim: achieve reasonable competency in C embedded coding and developing for stm32 microcontrollers.

## Devices Used

 - STM32 Nucleo-144 board with MCU : STM32F207ZGT6U.
 - sparkfun 9DOF IMU.
 - sparkfun micro barometer.

## Project Objectives

 - Learn freeRTOS concepts
 - Sensor study
    - sparkfun 9DOF IMU : includes 3 axis accelerometer, gyroscope and magnetometer compass.
        - link: https://www.sparkfun.com/products/15335
        - datasheet: https://cdn.sparkfun.com/assets/7/f/e/c/d/DS-000189-ICM-20948-v1.3.pdf
    - sparkfun micro lps28dfw barometer : pressure and temperature barometer
        - link: https://www.sparkfun.com/products/21222
        - datasheet: https://cdn.sparkfun.com/assets/a/4/0/b/b/LPS28DFW-Datasheet.pdf

## Project folders

sensors/               # STM32 CubeIDE project folders
├── Core/              # STM32 CubeMX-generated code and startup files
│   ├── Inc/           # Core header files (stm32f2xx_hal.h, main.h)
│   └── Src/           # Core source files (main.c, stm32f2xx_hal.c)
│
├── Drivers/           # Sensor drivers for ICM-20948 and LPS28DFW and I2C/SPI abstraction
│   ├── icm20948
│   │   ├── Inc/       # Driver header files
│   │   └── Src/       # Driver source files
│   ├── lps28dfw
│   │   ├── Inc/       # Driver header files
│   │   └── Src/       # Driver source files
│   ├── CMSIS
│   │   ├── Inc/       # Driver header files
│   │   └── Src/       # Driver source files
│   ├── STM32F2xx_HAL_Drivers
│   │   ├── Inc/       # Driver header files
│   │   └── Src/       # Driver source files
│
├── Middleware/        # Algorithms and third-party libraries
│   ├── Inc/           # Middleware header files (e.g., sensor fusion algorithms)
│   └── Src/           # Middleware source files
│
├── Config/            # Configuration files (sensor settings, pin configurations)
├── Lib/               # Reusable library files
│   ├── Inc/           # Library header files (public API)
│   └── Src/           # Library source files (implementation)
│
├── Tests/             # Unit tests, simulations, or test applications
├── Readme.md          # Project documentation
└── Makefile           # Build script