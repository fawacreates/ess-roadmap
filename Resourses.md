# ESS Master Learning Resources

This document contains the learning resources specified in the Zero → Expert Embedded Systems Software Engineer Planner.

Resources are organized by learning phase and difficulty so they can be used alongside the roadmap.

---

# Phase 1 — C Programming

## Basic C

### Textbook

**The C Programming Language — Brian W. Kernighan & Dennis M. Ritchie**

Primary textbook for learning C fundamentals.

Recommended topics:

* Data types
* Variables
* Constants
* Operators
* Control flow
* Functions
* Arrays
* Strings
* Basic program structure

### YouTube

**freeCodeCamp.org — C Programming Tutorial for Beginners**

Full beginner-oriented C course.

Link:

https://www.youtube.com/watch?v=KJgsSFOSQv0

### YouTube

**Neso Academy — C Programming**

Useful for short conceptual explanations and topic-by-topic revision.

Search:

`Neso Academy C Programming`

### Course

**CS50's Introduction to Computer Science — Harvard**

Use the early weeks for C foundations.

Link:

https://cs50.harvard.edu/x/

### Practice

* HackerRank C domain
* LeetCode Easy problems using C

### Basic Project

Console Calculator + Student Grade Manager

---

# Phase 1 — Intermediate C

## Pointers, Memory and Modular C

### Textbooks

**Expert C Programming: Deep Secrets — Peter van der Linden**

Focus on deeper C behavior, pointers, memory and common language pitfalls.

**Making Embedded Systems — Elecia White**

Use the early chapters as an introduction to applying C concepts in embedded systems.

### YouTube

**Miro Samek — Modern Embedded Systems Programming**

Topics include:

* Pointers
* Stack
* Bitwise operations
* Volatile
* Embedded C concepts

Playlist:

https://www.youtube.com/playlist?list=PLPW8O6W-1chwyTzI3BHwBLbGQoPFxPAPM

Companion site:

https://www.state-machine.com/video-course

### Course

**FastBit Embedded Brain Academy — Embedded C Programming**

Structured Embedded C training.

The planner lists this as a paid Udemy resource.

### GitHub Practice

Create a personal repository containing:

* Pointer exercises
* Bit-manipulation exercises
* C practice programs
* Experiments with memory and data structures

### Intermediate Project

Dynamic Student Database

Recommended concepts:

* Structures
* Linked lists or dynamic arrays
* Dynamic memory
* Bit-field status flags
* Modular `.c` / `.h` design
* Makefile
* Memory ownership

---

# Phase 1 — Expert C

## Robust, Portable and Optimized C

### Textbook

**Test-Driven Development for Embedded C — James W. Grenning**

Use for:

* TDD
* Embedded testing
* Design
* Testable C code

### Coding Standard

**Barr Group — Embedded C Coding Standard**

Use as a reference for developing safer and more consistent embedded C.

### Testing

**Unity**

C unit-testing framework.

### Mocking

**CMock**

Use alongside Unity for testing code with dependencies.

### Reference

**Modern C — Jens Gustedt**

Use as a deeper C reference.

### Expert Project

Refactor the intermediate C project using:

* TDD
* Unit tests
* Memory pool allocator
* Embedded C coding standards
* Portable C practices
* Design documentation

---

# Phase 2 — Computer Architecture and OS Basics

## Basic Level

### YouTube

**Ben Eater — Build an 8-bit Computer**

Useful for visualizing:

* CPU operation
* Registers
* Memory
* Instruction execution
* Digital computer architecture

Search:

`Ben Eater 8-bit computer`

### YouTube

**Neso Academy — Computer Organization & Architecture**

Use for structured computer architecture concepts.

### Project

Endianness detection and manual byte swapping program.

---

# Phase 2 — Intermediate Level

### Textbook

**Embedded Systems: Introduction to ARM Cortex-M Microcontrollers — Jonathan Valvano**

Volume 1.

Resources and code:

http://users.ece.utexas.edu/~valvano/

### YouTube

**Miro Samek**

Focus on:

* Stack
* Functions
* Procedure calls
* Calling conventions
* Generated machine behavior

### Project

C-to-Assembly Analysis

Use:

* `objdump`
* Compiler Explorer

Analyze a simple C function and explain the generated assembly.

---

# Phase 2 — Expert Level

### GitHub

**Arm University — Embedded Systems Fundamentals**

Repository:

https://github.com/arm-university/Embedded-Systems-Fundamentals

### Official ARM Documentation

Use the appropriate Cortex-M Generic User Guide for the processor being studied.

Topics:

* Core registers
* Special registers
* Exceptions
* NVIC
* Vector table
* Startup
* Linker scripts

### Course

**Embedded Software and Hardware Architecture — University of Colorado Boulder**

Coursera:

https://www.coursera.org/learn/embedded-software-hardware

### Project

Cortex-M Reset-to-Main Technical Note

Explain:

```text
Power-On Reset
      ↓
Vector Table
      ↓
Reset Handler
      ↓
Stack Initialization
      ↓
Startup Code
      ↓
System Initialization
      ↓
main()
```

---

# Phase 3 — Microcontrollers and Bare-Metal Programming

## Arduino

### Official Arduino Tutorials

https://www.arduino.cc/en/Tutorial/HomePage

Start with:

* Blink
* Button
* AnalogReadSerial
* Fade

### YouTube

**Paul McWhorter**

Complete Arduino tutorial series.

### YouTube

**DroneBot Workshop**

Useful for:

* Arduino
* Sensors
* Hardware interfaces
* Practical embedded projects

### Basic Project

Temperature and humidity monitor.

---

# Phase 3 — STM32

## Courses

**FastBit Embedded Brain Academy**

Relevant areas:

* ARM Cortex-M3/M4
* STM32
* Embedded Systems Programming
* Bare-metal programming

### YouTube

**Controllerstech**

Practical STM32 tutorials covering:

* HAL
* Register-level programming
* Peripherals
* STM32 development

Channel:

https://www.youtube.com/@Controllerstech

### YouTube

**Miro Samek**

Use for deeper understanding of:

* GPIO
* Peripherals
* Embedded architecture
* Low-level programming

### GitHub

**Controllerstech STM32**

https://github.com/controllerstech/STM32

### GitHub

**Quantum Leaps — Modern Embedded Programming Course**

https://github.com/QuantumLeaps/modern-embedded-programming-course

### Textbook

**Mastering STM32 — Carmine Noviello**

Alternative:

**Jonathan Valvano Embedded Systems books**

### Official Resources

Use:

* STMicroelectronics documentation
* STM32CubeMX
* STM32 example packages
* STM32 reference manuals
* STM32 datasheets

### Intermediate Project

STM32 Multi-Sensor Node.

### Expert Project

DMA-based Sensor Logger with:

* DMA
* UART
* Low-power operation
* Serial command interface

---

# Phase 4 — Communication Protocols

## YouTube

**Andreas Spiess**

Topics:

* Sensors
* ESP32
* IoT
* Wireless communication
* Embedded networking

https://www.youtube.com/@AndreasSpiess

### Website

**Random Nerd Tutorials**

Topics:

* ESP32
* Sensors
* IoT
* Wireless communication

https://randomnerdtutorials.com/

### Hardware

**ESP32 DevKit**

Use for:

* Wi-Fi
* Bluetooth
* MQTT
* IoT experiments

### GitHub

**ESP-IDF Examples**

Use the official Espressif examples for ESP32 development.

### Logic Analyzer

Recommended:

* 8-channel USB logic analyzer
* PulseView / Sigrok

Alternative:

* Saleae logic analyzer

### Projects

#### Basic

I2C temperature sensor + SPI OLED.

#### Intermediate

UART command parser with:

* CRC
* Multiple peripherals
* Error handling

#### Expert

ESP32 IoT node:

```text
Sensor
   ↓
ESP32
   ↓
Wi-Fi
   ↓
MQTT Broker
   ↓
Client / Application
```

---

# Phase 5 — Real-Time Operating Systems

## Official FreeRTOS

https://www.freertos.org/

Use for:

* API reference
* Documentation
* Kernel information
* LTS releases

### Free Book

**Mastering the FreeRTOS Real Time Kernel**

GitHub:

https://github.com/FreeRTOS/FreeRTOS-Kernel-Book

### YouTube

**Miro Samek — RTOS lessons**

Use alongside the Modern Embedded Systems Programming material.

### GitHub

**FreeRTOS**

https://github.com/FreeRTOS/FreeRTOS

### GitHub

**FreeRTOS Kernel**

https://github.com/FreeRTOS/FreeRTOS-Kernel

### Intermediate Resources

Continue:

* Mastering the FreeRTOS Real Time Kernel
* Official FreeRTOS API documentation
* STM32 FreeRTOS examples

The planner specifically mentions Controllerstech FreeRTOS material and community examples.

### System Visualization

**SEGGER SystemView**

Use to visualize:

* Task execution
* Scheduling
* Interrupts
* Timing
* RTOS behavior

The planner notes that it is available free for non-commercial use.

### Expert Textbook

**Hands-On RTOS with Microcontrollers — Brian Amos**

### Alternative RTOS

**Zephyr Project**

https://www.zephyrproject.org/

Use later for comparison with FreeRTOS.

### Projects

#### Basic

Three independent LED tasks.

#### Intermediate

```text
Sensor Task
     ↓
FreeRTOS Queue
     ↓
Processing Task
     ↓
UART Task
```

#### Expert

Multi-task environmental monitoring system with:

* Synchronization
* Static allocation where possible
* Command interface
* Logging
* SystemView traces

---

# Phase 6 — Electronics

## Beginner Electronics

### Book

**Make: Electronics — Charles Platt**

Primary beginner-friendly practical electronics resource.

### YouTube

**GreatScott!**

### YouTube

**Afrotechmods**

### YouTube

**EEVblog**

Use these for practical electronics concepts and lab techniques.

### Project

Build and measure:

* Voltage divider
* RC low-pass filter

Compare measured values with theoretical calculations.

---

# Phase 6 — Intermediate Electronics

### Reference Book

**The Art of Electronics — Horowitz & Hill**

Long-term electronics reference.

### YouTube

**EEVblog**

Useful for practical electronics and measurement.

### YouTube

**Phil's Lab**

Useful for:

* Schematics
* PCB design
* Embedded hardware
* Practical engineering

### Tool

**KiCad**

Free, professional-grade EDA software.

https://www.kicad.org/

### Project

MCU-controlled transistor switch.

Design the schematic in KiCad.

---

# Phase 6 — Advanced Hardware

### YouTube

**Phil's Lab**

Focus on:

* PCB design
* Decoupling
* Ground planes
* Signal integrity
* Power distribution
* Embedded hardware design

### Tool

**KiCad**

Use for:

```text
Schematic
    ↓
Footprints
    ↓
PCB Layout
    ↓
Design Review
    ↓
Gerbers
```

### Project

Two-layer STM32 or ESP32 sensor PCB.

If budget allows:

* Manufacture the PCB
* Assemble it
* Test it

Otherwise:

* Complete the schematic
* Complete PCB layout
* Generate Gerbers
* Review the design

---

# Phase 7 — Embedded Linux and Professional Practices

## Embedded Linux Hardware

Recommended:

* Raspberry Pi
* BeagleBone Black

Use one as an Embedded Linux learning platform.

### Linux

Become comfortable with:

* Linux command line
* Filesystems
* Processes
* Permissions
* Shell commands
* Compilation
* Networking

### Buildroot

Study:

* Minimal Linux systems
* Root filesystem
* Kernel
* Boot process
* Cross-compilation
* Embedded deployment

### YouTube / Search Topics

Search for:

`Buildroot tutorial`

`Yocto Project getting started`

`OpenOCD GDB STM32`

### ARM Learning Paths

https://learn.arm.com/

### Development Tools

Learn:

* GCC
* Cross-compilers
* Make
* Git
* GDB
* OpenOCD

### Static Analysis

Recommended tools from the planner:

* cppcheck
* clang-tidy
* Vendor static-analysis tools

### Unit Testing

Recommended:

* Unity
* CMock
* Ceedling

### GitHub Resource

**Awesome Embedded**

https://github.com/nhivp/Awesome-Embedded

### Professional Practices

Study:

* Coding standards
* Static analysis
* Unit testing
* Continuous integration
* Technical documentation
* Design documents
* Secure coding
* Secure boot concepts
* Buffer-overflow prevention

### Project

Take an earlier STM32 project and add:

* Unit tests
* Automated build
* Static analysis
* Professional README
* Architecture document

---

# Phase 8 — Specialization and Job Readiness

## Domains

The planner recommends choosing **1–2 domains** for deeper study.

Possible areas listed:

* IoT / Consumer
* Automotive
* Industrial
* Robotics
* Medical devices

The repository can later document the chosen specialization separately.

## Portfolio Projects

Recommended project directions from the planner:

### RTOS Environmental Monitor

Demonstrate:

* RTOS
* Multiple sensors
* Communication
* MQTT or UART logging
* Structured software architecture

### Custom Bootloader

Demonstrate:

* Firmware update mechanism
* UART or USB
* Flash memory
* Application handoff

### Motor Control / PID

Demonstrate:

* STM32
* Control systems
* PWM
* Sensors
* FreeRTOS

### ESP32 IoT Gateway

Demonstrate:

* Sensors
* ESP32
* Networking
* Cloud communication

### CAN Bus Node

Demonstrate:

* CAN communication
* Embedded networking
* Automotive-style diagnostics

---

# Certifications and Credentials

Certifications are optional in the planner.

Possible resources include:

### Coursera / edX

Embedded Systems specializations, including University of Colorado Boulder or similar programs.

### FreeRTOS / AWS IoT

Training and qualification paths through:

* FreeRTOS
* AWS Training

### Arm

Courses and badges through:

https://learn.arm.com/

### Vendor Training

Training certificates from vendors such as:

* ST
* TI
* NXP

when available.

The planner specifically treats certifications as supplementary rather than as a replacement for practical projects and a strong GitHub portfolio.

---

# Master YouTube List

The planner's main recommended channels are:

1. **Quantum Leaps / Miro Samek**

   * Modern Embedded Systems Programming
   * Deep embedded fundamentals
   * RTOS
   * State machines
   * Low-level programming

   https://www.youtube.com/playlist?list=PLPW8O6W-1chwyTzI3BHwBLbGQoPFxPAPM

2. **FastBit Embedded Brain Academy**

   * Embedded C
   * ARM Cortex-M
   * STM32
   * FreeRTOS

3. **Controllerstech**

   * STM32
   * HAL
   * Register-level programming

4. **Phil's Lab**

   * PCB design
   * Embedded hardware
   * Advanced electronics

5. **Andreas Spiess**

   * ESP32
   * Sensors
   * IoT
   * Communication

6. **EEVblog**

   * Electronics
   * Measurement
   * Engineering practice

7. **GreatScott!**

   * Electronics
   * Practical circuits

8. **Ben Eater**

   * Computer architecture
   * CPU fundamentals

9. **DroneBot Workshop**

   * Arduino
   * Sensors
   * Embedded hardware

10. **Paul McWhorter**

    * Arduino
    * Beginner microcontroller projects

---

# Master GitHub Resources

### Quantum Leaps — Modern Embedded Programming Course

https://github.com/QuantumLeaps/modern-embedded-programming-course

### FreeRTOS

https://github.com/FreeRTOS/FreeRTOS

### FreeRTOS Kernel

https://github.com/FreeRTOS/FreeRTOS-Kernel

### FreeRTOS Kernel Book

https://github.com/FreeRTOS/FreeRTOS-Kernel-Book

### Awesome Embedded

https://github.com/nhivp/Awesome-Embedded

### Arm University — Embedded Systems Fundamentals

https://github.com/arm-university/Embedded-Systems-Fundamentals

### Controllerstech STM32

https://github.com/controllerstech/STM32

---

# Master Textbook List

| Area        | Resource                                                | Primary Use                   |
| ----------- | ------------------------------------------------------- | ----------------------------- |
| C           | The C Programming Language — K&R                        | C foundations                 |
| C           | Expert C Programming — Peter van der Linden             | Advanced C                    |
| Embedded C  | Making Embedded Systems — Elecia White                  | Embedded C thinking           |
| Embedded C  | Test-Driven Development for Embedded C — James Grenning | Testing and design            |
| C Reference | Modern C — Jens Gustedt                                 | Advanced C reference          |
| ARM / MCU   | Embedded Systems — Jonathan Valvano                     | Cortex-M and embedded systems |
| STM32       | Mastering STM32 — Carmine Noviello                      | STM32 development             |
| RTOS        | Mastering the FreeRTOS Real Time Kernel                 | FreeRTOS                      |
| RTOS        | Hands-On RTOS with Microcontrollers — Brian Amos        | RTOS development              |
| Electronics | Make: Electronics — Charles Platt                       | Beginner electronics          |
| Electronics | The Art of Electronics — Horowitz & Hill                | Long-term reference           |

---

# Online Course List

## C

* CS50
* freeCodeCamp C course
* Neso Academy C material

## Embedded C / STM32

* FastBit Embedded Brain Academy
* Miro Samek Modern Embedded Systems Programming
* Controllerstech STM32 tutorials

## ARM

* Arm Learning Paths
* University of Colorado Boulder — Embedded Software and Hardware Architecture

## RTOS

* FreeRTOS official training/documentation
* Mastering the FreeRTOS Real Time Kernel
* Miro Samek RTOS material
* Brian Amos RTOS material

## Embedded Linux

* Buildroot tutorials
* Yocto Project getting-started material
* Arm Learning Paths

---

# Hardware Progression

The planner recommends purchasing hardware progressively rather than all at once.

```text
1. Arduino Uno / Nano
        ↓
2. STM32 Nucleo / Blue Pill
        ↓
3. ESP32 DevKit
        ↓
4. Logic Analyzer + Multimeter
        ↓
5. Raspberry Pi
        ↓
6. Optional Oscilloscope
        ↓
7. Custom PCB
```

Hardware should be introduced as the corresponding concepts are learned.

---

# Recommended Resource Workflow

For each topic:

```text
Choose Resource
      ↓
Study
      ↓
Practice Immediately
      ↓
Build Mini Project
      ↓
Debug
      ↓
Document
      ↓
Commit to GitHub
```

The planner explicitly recommends working on one chunk at a time and not rushing to the next level until the associated project can be completed confidently.

---

# Resource Selection Rule

The planner contains multiple resources for the same subject.

They should not all be completed from beginning to end.

Use:

**Primary Resource → Practice → Project → Secondary Resource for clarification → Documentation / Reference**

The goal is implementation and understanding rather than collecting courses or certificates.

---

# Hardware Philosophy

The planner recommends hardware practice early because theory without practical hardware experience is less effective for embedded learning.

The intended progression is:

```text
Software
   ↓
Arduino
   ↓
STM32
   ↓
Protocols
   ↓
RTOS
   ↓
Electronics
   ↓
Embedded Linux
   ↓
Professional Embedded Systems
```

---

# Core Resource Principle

The repository should treat the resources as tools for completing the roadmap, not as a checklist of courses.

The primary objective is:

```text
Learn
  ↓
Understand
  ↓
Practice
  ↓
Build
  ↓
Debug
  ↓
Document
  ↓
Repeat
```
