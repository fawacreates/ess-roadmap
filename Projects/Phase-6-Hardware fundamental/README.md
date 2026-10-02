# Phase 6 — Hardware Fundamentals

Projects focused on developing the electronics knowledge required to design, measure, debug, and integrate hardware with embedded systems.

## Projects

### 1. Voltage Divider

Status: Not Started

#### Architecture

```text
              VCC
               |
              R1
               |
               +---------> VOUT
               |
              R2
               |
              GND
```

Measurement flow:

```text
Voltage Source
      |
      v
Voltage Divider
      |
      v
Output Voltage
      |
      v
Multimeter Measurement
      |
      v
Compare:
Calculated VOUT
      |
      +
Measured VOUT
```

#### Hardware Requirements

* Breadboard
* Resistors with multiple values
* DC power source
* Jumper wires
* Multimeter
* Breadboard power supply — optional
* Oscilloscope — optional

#### Software Requirements

* Calculator or spreadsheet software
* KiCad — recommended for schematic documentation
* Git
* GitHub repository
* Text editor or Markdown editor

#### Topics

* Ohm's Law
* Voltage
* Current
* Resistance
* Series circuits
* Voltage dividers
* Electrical measurements
* Measurement error

#### Completion Criteria

The project is complete when:

1. A voltage-divider circuit is calculated before construction.
2. The resistor values are documented.
3. The expected output voltage is calculated.
4. The circuit is built successfully.
5. At least **3 different input voltages or resistor configurations** are tested.
6. At least **3 voltage measurements** are recorded.
7. Measured values are compared with calculated values.
8. Measurement differences are documented.
9. At least **1 unexpected result or measurement problem** is investigated.
10. The circuit schematic is documented.
11. The project can be reproduced from the documentation.

---

### 2. RC Low-Pass Filter

Status: Not Started

#### Architecture

```text
                    R
VIN --------/\/\/\/\--------+-------- VOUT
                            |
                            C
                            |
                           GND
```

Signal flow:

```text
Input Signal
     |
     v
   Resistor
     |
     +------> Output
     |
  Capacitor
     |
     v
    GND
```

Frequency-response concept:

```text
Low Frequency
      |
      v
Signal passes
      |
      v
Higher Frequency
      |
      v
Signal attenuation increases
```

#### Hardware Requirements

* Breadboard
* Resistors
* Capacitors
* Signal generator or suitable waveform source
* Jumper wires
* Multimeter
* Oscilloscope
* Breadboard power supply — if required

#### Software Requirements

* KiCad
* Calculator or spreadsheet software
* Oscilloscope analysis software — if applicable
* Git
* GitHub repository
* Text editor or Markdown editor

#### Topics

* Capacitors
* RC circuits
* Time constants
* Frequency response
* Cutoff frequency
* Signal filtering
* Oscilloscope measurements

#### Completion Criteria

The project is complete when:

1. The RC filter is mathematically designed before construction.
2. The resistor and capacitor values are documented.
3. The expected cutoff frequency is calculated.
4. The circuit is built successfully.
5. At least **5 different input frequencies** are tested.
6. Input and output signals are measured.
7. At least **5 measurement results** are documented.
8. The measured frequency response is compared with the expected behavior.
9. The cutoff region is identified.
10. At least **1 measurement or circuit problem** is investigated.
11. The schematic and measurement setup are documented.

---

### 3. MCU-Controlled Transistor Switch

Status: Not Started

#### Architecture

```text
                 VCC
                  |
               LOAD
                  |
                  +------+
                         |
                       Drain
                    +---------+
MCU GPIO ----R----->|  MOSFET |
                    +---------+
                       Source
                         |
                        GND
```

Control flow:

```text
MCU GPIO
    |
    v
Gate Control
    |
    v
MOSFET
    |
    v
Load ON / OFF
```

Software-to-hardware interaction:

```text
C Program
    |
    v
GPIO Configuration
    |
    v
GPIO Output
    |
    v
MOSFET Gate
    |
    v
Electrical Load
```

#### Hardware Requirements

* STM32 development board
* Logic-level MOSFET
* Suitable load such as LED, small motor, or other low-voltage load
* Gate resistor where appropriate
* Pull-down resistor where appropriate
* Breadboard
* Jumper wires
* External power supply if required by the load
* Multimeter
* Oscilloscope — recommended
* Flyback diode for inductive loads where applicable

#### Software Requirements

* STM32CubeIDE
* STM32CubeMX — included with or integrated into the STM32 development workflow
* STM32 HAL/CMSIS libraries
* C compiler/toolchain provided by STM32CubeIDE
* Git
* GitHub repository
* Serial terminal — optional

#### Topics

* Transistors
* MOSFETs
* GPIO
* Switching
* Gate control
* Pull-up/pull-down concepts
* Load driving
* Datasheets
* Electrical measurements
* MCU-to-hardware interfacing

#### Completion Criteria

The project is complete when:

1. The MOSFET is selected using its datasheet specifications.
2. The load requirements are documented.
3. The circuit schematic is completed before construction.
4. The MCU successfully controls the MOSFET.
5. The load switches between the required states reliably.
6. At least **20 ON/OFF switching cycles** are tested.
7. GPIO behavior is verified using a measurement or debugging method.
8. Voltage measurements are recorded at relevant points.
9. At least **1 hardware or switching problem** is investigated and resolved.
10. The MOSFET's relevant electrical specifications are documented.
11. The circuit can be reproduced from the documentation.

---

### 4. STM32/ESP32 Two-Layer PCB

Status: Not Started

#### Architecture

```text
                    Embedded System
                          |
              +-----------+-----------+
              |                       |
              v                       v
        Microcontroller          External Hardware
              |                       |
              +-----------+-----------+
                          |
                          v
                    PCB Interface
                          |
              +-----------+-----------+
              |                       |
              v                       v
        Power Distribution       Signal Routing
              |                       |
              +-----------+-----------+
                          |
                          v
                    External Connectors
```

PCB development flow:

```text
Requirements
     |
     v
Schematic
     |
     v
Component Selection
     |
     v
PCB Layout
     |
     v
Design Rule Check
     |
     v
Manufacturing Files
     |
     v
PCB Fabrication
     |
     v
Assembly
     |
     v
Electrical Testing
     |
     v
Firmware Testing
```

Layer concept:

```text
+--------------------------------------+
| Top Layer                            |
| Components + Signal Routing         |
+--------------------------------------+
| Bottom Layer                         |
| Ground / Signal Routing              |
+--------------------------------------+
```

#### Hardware Requirements

* STM32 or ESP32 development platform
* Selected sensors/modules
* PCB components
* Resistors
* Capacitors
* Connectors
* LEDs where required
* Voltage regulator/power circuitry where required
* USB or programming interface as required
* Multimeter
* Soldering equipment
* PCB fabrication service
* Logic analyzer — recommended
* Oscilloscope — recommended

#### Software Requirements

* KiCad
* STM32CubeIDE or ESP32 development environment
* Required MCU SDK/HAL/framework
* C compiler/toolchain
* Git
* GitHub repository
* PCB manufacturer design-rule documentation
* Gerber viewer

#### Topics

* Schematics
* PCB design
* Component selection
* Datasheets
* PCB layers
* Ground planes
* Power distribution
* Signal routing
* Design rules
* Design Rule Check
* Gerber files
* PCB fabrication
* Assembly
* Electrical testing
* Signal integrity

#### Completion Criteria

The project is complete when:

1. The complete system requirements are documented.
2. All major components are selected using their datasheets.
3. The schematic is complete.
4. Electrical connections are reviewed before PCB layout.
5. PCB layout is completed.
6. Design Rule Check passes with no unresolved critical errors.
7. Manufacturing files are generated successfully.
8. The PCB is fabricated.
9. Components are assembled correctly.
10. Power rails are tested before connecting the MCU.
11. At least **5 meaningful electrical measurements** are recorded during bring-up.
12. The MCU can be programmed successfully.
13. Required peripherals operate correctly.
14. At least **1 PCB hardware problem** is investigated and resolved.
15. The final PCB revision is documented.
16. The schematic, PCB layout, manufacturing files, and firmware are organized in the repository.
17. The project can be reproduced from the documentation.

---

## Common Hardware and Documentation Requirements

For every electronics project:

* Document the exact components used.
* Record relevant component part numbers.
* Consult datasheets before construction.
* Document operating voltage and current requirements.
* Document resistor, capacitor, and other component values.
* Include a schematic.
* Document wiring and connections.
* Record important measurements.
* Compare calculated and measured values where applicable.
* Include photographs of physical circuits where useful.
* Document hardware problems and their solutions.
* Verify power and polarity before energizing a circuit.

## Common Software Requirements

For every project:

* Use Git for version control.
* Record software versions where applicable.
* Document calculation tools used.
* Keep schematics and design files in the repository.
* Keep generated build artifacts out of the repository.
* Document firmware build and flashing procedures where applicable.
* Do not commit passwords, API keys, or other secrets.
* Keep the README sufficient for another person to reproduce the project.

## Hardware Documentation Requirements

Every hardware project should document:

* System architecture
* Schematic
* Component selection
* Datasheet references
* Electrical calculations
* Expected behavior
* Measured behavior
* Test equipment
* Test procedure
* Measurement results
* Problems encountered
* Debugging process
* Final design
* Possible improvements

## Project Status

Use these status values:

```text
NOT STARTED
    ↓
IN PROGRESS
    ↓
TESTING
    ↓
PASS
```

If a completion criterion is not met:

```text
TESTING
    ↓
FAIL / INCOMPLETE
    ↓
FIX
    ↓
RETEST
    ↓
PASS
```

A project should only be marked **PASS** when all mandatory completion criteria have been satisfied.
