# EnviroTrack_F4

## Real-Time Environmental Monitoring System using STM32F407

This project is a firmware-based environmental monitoring simulation built on the STM32F407VGT6 microcontroller. It demonstrates real-time embedded system design using UART communication and timer interrupts.

## Project Overview

The system simulates temperature and humidity sensor values and transmits them periodically through USART2 using timer-driven interrupts.

This project focuses on:

* Timer interrupt configuration
* UART serial communication
* Sensor simulation logic
* Real-time data transmission
* Embedded firmware development using STM32 HAL

---

## Features

* Simulated temperature and humidity monitoring
* Periodic data transmission every 1 second
* UART communication at 115200 baud
* Timer interrupt-driven execution using TIM2
* Automatic threshold reset mechanism

---

## Hardware / Platform

* STM32F407VGT6
* STM32CubeMX
* STM32CubeIDE
* STM32 HAL Library

---

## Peripherals Used

### USART2

Used for serial communication.

Configuration:

* Baud Rate: 115200
* Word Length: 8 bits
* Parity: None
* Stop Bits: 1

Pins:

* PA2 → TX
* PA3 → RX

---

### TIM2

Used to generate periodic interrupts.

Configuration:

* Prescaler: 8399
* Counter Period: 999
* Interrupt Frequency: 1 second

---

## Project Workflow

1. Initialize system clock
2. Initialize GPIO, USART2, and TIM2
3. Start TIM2 interrupt
4. Generate simulated sensor values
5. Format data using sprintf()
6. Transmit data via UART

---

## Sample Output

Temp: 25 C | Humidity: 60 %
Temp: 26 C | Humidity: 62 %
Temp: 27 C | Humidity: 64 %
Temp: 28 C | Humidity: 66 %

---

## Project Structure

EnviroTrack_F4/
├── Core/
├── Drivers/
├── images/
├── EnviroTrack_F4.ioc
├── README.md

---

## Screenshots

### CubeMX Pin Configuration

Shows USART2 and TIM2 setup.

### USART2 Configuration

Shows UART communication settings.

### TIM2 Configuration

Shows timer interrupt settings.

### Firmware Logic

Main program and interrupt callback.

### Build Success

Successful project compilation.

---

## Future Improvements

* Add ADC sensor input
* Add real hardware sensor integration
* Add UART command-based control
* Add threshold alert system
* Add data logging support

---
