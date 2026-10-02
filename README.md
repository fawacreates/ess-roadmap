# Zero to Expert: Embedded Systems Software Engineer

A structured learning roadmap for progressing from BCA student to job-ready Embedded Systems Software Engineer.

This repository documents my long-term journey into Embedded Systems Software Engineering, starting from software foundations and progressing toward microcontrollers, bare-metal programming, communication protocols, RTOS, electronics, Embedded Linux, and professional embedded development.

The goal is to understand the fundamentals, build real systems, document the work, and progressively develop engineering-level skills.

## Goal

Build a strong foundation and practical portfolio across:

* C Programming
* Computer Architecture
* Operating System Fundamentals
* Microcontrollers
* Bare-Metal Programming
* Communication Protocols
* RTOS
* Electronics
* Embedded Linux
* Debugging and Development Tools
* Testing and Professional Practices
* Embedded Systems Projects

## Roadmap

### Phase 1 — Software Foundations

C Programming

Learn C from fundamentals through pointers, memory management, bit manipulation, modular programming, testing, portability, and embedded coding practices.

Projects:

* Console Calculator and Student Grade Manager
* Dynamic Student Database
* TDD-based C project with memory pool allocator

### Phase 2 — Computer Architecture and OS Basics

Build the mental model needed to understand what happens when C code executes on a microcontroller.

Topics:

* Binary and hexadecimal
* Two's complement
* Endianness
* CPU architecture
* Registers and ALU
* Memory hierarchy
* Stack frames
* Processes and threads
* Interrupts
* ARM Cortex-M architecture
* Vector tables
* Startup code
* Linker scripts
* CMSIS

Projects:

* Endianness detection and byte swapping
* C-to-assembly analysis
* Cortex-M reset-to-main technical note

### Phase 3 — Microcontrollers and Bare-Metal Programming

Move from software into embedded hardware.

Progression:

Arduino → STM32 → Register-Level Programming → Drivers → DMA → Low Power → Bootloaders

Topics:

* GPIO
* Interrupts
* Timers
* PWM
* ADC
* UART
* I2C
* SPI
* DMA
* Low-power modes
* SWD/JTAG debugging
* Peripheral drivers
* Bootloaders

Projects:

* Temperature and humidity monitor
* STM32 multi-sensor node
* DMA-based sensor logger
* Custom bootloader

### Phase 4 — Communication Protocols and Interfacing

Understand how embedded systems communicate with sensors, peripherals, and other devices.

Protocols:

* UART
* I2C
* SPI
* CAN
* Wi-Fi
* Bluetooth

Additional concepts:

* CRC
* ACK/NACK
* Retries
* Sequence numbers
* Ring buffers
* Timing diagrams
* Logic-analyzer debugging

Projects:

* I2C sensor and SPI OLED
* UART command parser with CRC
* ESP32 MQTT IoT node

### Phase 5 — Real-Time Operating Systems

Learn how embedded applications move beyond simple super-loops into structured real-time systems.

Topics:

* FreeRTOS
* Tasks
* Scheduling
* Task states
* Queues
* Semaphores
* Mutexes
* Priority inheritance
* Task notifications
* Software timers
* Event groups
* Stream and message buffers
* Tickless idle
* Static allocation
* State machines

Projects:

* Multi-task LED system
* Sensor → Queue → Processing → UART architecture
* Multi-task environmental monitoring system

### Phase 6 — Hardware Fundamentals

Develop enough hardware knowledge to confidently work with embedded systems.

Topics:

* Ohm's Law
* Kirchhoff's Laws
* Resistors
* Capacitors
* Inductors
* Diodes
* LEDs
* Transistors
* MOSFETs
* Op-amps
* Datasheets
* Schematics
* PCB design
* Signal integrity
* Power distribution
* ADC considerations

Tools:

* Multimeter
* Logic analyzer
* Oscilloscope
* KiCad

Projects:

* Voltage divider
* RC low-pass filter
* MCU-controlled transistor switch
* STM32/ESP32 two-layer PCB

### Phase 7 — Embedded Linux and Professional Practices

Move toward professional embedded development workflows.

Topics:

* Linux command line
* ARM cross-compilation
* Buildroot
* Git
* Advanced Git workflows
* GDB
* OpenOCD
* Device trees
* Static analysis
* Unit testing
* Continuous integration
* Technical documentation
* Secure coding

Project:

Build a minimal Buildroot Embedded Linux image that runs a custom C application and communicates through UART or a network.

### Phase 8 — Specialization and Job Readiness

Turn the accumulated knowledge into a professional portfolio.

Focus areas:

* IoT / Consumer
* Automotive
* Industrial
* Medical devices

Portfolio goals:

Build and polish 4–6 substantial embedded projects demonstrating:

* Bare-metal programming
* RTOS
* Communication protocols
* Sensors
* Clean C
* Debugging
* Testing
* Documentation

Also develop:

* Open-source contributions
* Embedded interview preparation
* Driver-design practice
* RTOS problem solving
* Bit manipulation skills
* Technical communication

## Repository Structure

```text
ess-engineer-roadmap/
│
├── README.md
│
├── docs/
│   └── ESS_Engineer_Zero_to_Expert_Planner.pdf
│
├── projects/
│   ├── phase-01-c-programming/
│   ├── phase-02-computer-architecture/
│   ├── phase-03-microcontrollers/
│   ├── phase-04-communication-protocols/
│   ├── phase-05-rtos/
│   ├── phase-06-electronics/
│   ├── phase-07-embedded-linux/
│   └── phase-08-portfolio/
│
├── notes/
│   ├── c/
│   ├── computer-architecture/
│   ├── microcontrollers/
│   ├── protocols/
│   ├── rtos/
│   ├── electronics/
│   └── embedded-linux/
│
└── resources/
    └── resources.md
```

## Core Resources

### C and Embedded C

* The C Programming Language — Brian W. Kernighan and Dennis M. Ritchie
* Expert C Programming: Deep Secrets — Peter van der Linden
* Making Embedded Systems — Elecia White
* Modern Embedded Systems Programming — Quantum Leaps / Miro Samek

### Microcontrollers

* Jonathan Valvano — Embedded Systems series
* Mastering STM32 — Carmine Noviello
* STMicroelectronics documentation
* Controllerstech STM32 tutorials

### RTOS

* Mastering the FreeRTOS Real Time Kernel
* Hands-On RTOS with Microcontrollers — Brian Amos
* FreeRTOS documentation
* Miro Samek's RTOS material

### Electronics

* Make: Electronics — Charles Platt
* The Art of Electronics — Horowitz and Hill
* Phil's Lab
* EEVblog
* GreatScott!

### Embedded Linux

* Arm Learning Paths
* Buildroot
* GDB
* OpenOCD

## Hardware Progression

The planned hardware progression is:

```text
Arduino
   ↓
STM32
   ↓
ESP32
   ↓
Logic Analyzer + Multimeter
   ↓
Raspberry Pi
   ↓
Oscilloscope
   ↓
Custom PCB
```

Hardware will be introduced progressively rather than purchased all at once.

## Progress

* [ ] Phase 1 — C Programming
* [ ] Phase 2 — Computer Architecture and OS
* [ ] Phase 3 — Microcontrollers and Bare Metal
* [ ] Phase 4 — Communication Protocols
* [ ] Phase 5 — RTOS
* [ ] Phase 6 — Electronics
* [ ] Phase 7 — Embedded Linux
* [ ] Phase 8 — Portfolio and Job Readiness

## Learning Log

| Date | Topic | What I Learned | Practice / Project | Status      |
| ---- | ----- | -------------- | ------------------ | ----------- |
| —    | —     | —              | —                  | Not Started |

This log will grow as the roadmap progresses.

## Learning Method

For every major topic:

Learn → Practice → Build → Debug → Document → Commit → Improve

The emphasis is on implementation.

Instead of only watching a tutorial:

1. Understand the concept.
2. Reproduce it yourself.
3. Modify the implementation.
4. Break it intentionally.
5. Debug the problem.
6. Document what happened.
7. Commit the result.

## Portfolio Philosophy

Every project should gradually become more professional.

Early projects may be small experiments.

Later projects should demonstrate:

```text
Clean C
   ↓
Hardware interaction
   ↓
Peripheral drivers
   ↓
Communication
   ↓
Real-time behavior
   ↓
Debugging
   ↓
Testing
   ↓
Documentation
   ↓
Production-style engineering
```

The objective is to build a portfolio that shows how I think and engineer, not simply how many tutorials I completed.

## Master Planner

The complete Zero to Expert ESS Engineer Planner is available here:

[ESS_Engineer_Zero_to_Expert_Planner.pdf](docs/ESS_Engineer_Zero_to_Expert_Planner.pdf)

## Long-Term Objective

Become a capable Embedded Systems Software Engineer by developing strong fundamentals, building progressively complex systems, gaining practical hardware experience, contributing to real projects, and maintaining a documented engineering portfolio.

> Consistency beats intensity. Build something. Document it. Understand it. Improve it.

