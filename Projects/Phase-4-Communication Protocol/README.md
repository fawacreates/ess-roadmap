# Phase 4 — Communication Protocols and Interfacing

Projects focused on understanding how embedded systems communicate with sensors, peripherals, and other devices.

## Projects

### 1. I2C Sensor and SPI OLED

Status: Not Started

#### Hardware Requirements

* STM32 development board
* I2C-compatible temperature/humidity sensor
* SPI-compatible OLED display
* Breadboard
* Jumper wires
* USB cable
* Logic analyzer — recommended for protocol verification
* Multimeter — recommended for checking power and connections

#### Software Requirements

* STM32CubeIDE
* STM32CubeMX — included with or integrated into the STM32 development workflow
* STM32 HAL/CMSIS libraries
* C compiler/toolchain provided by STM32CubeIDE
* Serial terminal — for debugging and output
* Git
* GitHub repository for source code and documentation
* Logic analyzer software — if a logic analyzer is used

#### Topics

* I2C communication
* SPI communication
* Sensor interfacing
* OLED interfacing
* Device addressing
* Data transmission
* Peripheral configuration

#### Completion Criteria

The project is complete when:

1. The sensor communicates successfully over I2C.
2. The OLED communicates successfully over SPI.
3. Sensor data is read correctly at least **20 consecutive times**.
4. The received sensor values are displayed correctly on the OLED.
5. At least **3 different sensor conditions or input values** are tested.
6. I2C communication is verified using a debugger, logic analyzer, or equivalent method where available.
7. SPI communication is verified using a debugger, logic analyzer, or equivalent method where available.
8. At least **1 communication or hardware problem** is investigated and resolved.
9. The I2C address, SPI configuration, wiring, and relevant peripheral settings are documented.
10. The project can be rebuilt and demonstrated using the README instructions.

---

### 2. UART Command Parser with CRC

Status: Not Started

#### Hardware Requirements

* STM32 development board
* USB-to-UART adapter, if required
* Computer
* Breadboard — if external connections are required
* Jumper wires
* USB cable
* Logic analyzer — recommended for inspecting UART traffic
* Multimeter — recommended for checking connections and voltage levels

#### Software Requirements

* STM32CubeIDE
* STM32CubeMX — included with or integrated into the STM32 development workflow
* STM32 HAL/CMSIS libraries
* C compiler/toolchain provided by STM32CubeIDE
* Serial terminal such as PuTTY, Tera Term, or a similar terminal
* Git
* GitHub repository
* Logic analyzer software — if a logic analyzer is used

#### Topics

* UART
* Serial communication
* Command parsing
* Ring buffers
* CRC
* ACK/NACK
* Error handling
* Data validation

#### Completion Criteria

The project is complete when:

1. UART communication works reliably at the documented baud rate and configuration.
2. At least **10 valid commands** are processed correctly.
3. At least **5 invalid or malformed commands** are tested.
4. Invalid commands are rejected without crashing the system.
5. CRC validation correctly accepts valid messages.
6. CRC validation correctly rejects corrupted messages.
7. ACK/NACK behavior is implemented and verified where applicable.
8. Ring-buffer behavior is tested with multiple incoming messages.
9. At least **1 communication or parsing bug** is investigated and resolved.
10. UART traffic and message format are documented with examples.
11. The project can be rebuilt and demonstrated using the README instructions.

---

### 3. ESP32 MQTT IoT Node

Status: Not Started

#### Hardware Requirements

* ESP32 development board
* Sensor compatible with the selected interface
* Breadboard
* Jumper wires
* USB cable
* Computer
* Wi-Fi network
* MQTT broker
* Logic analyzer — optional
* Multimeter — recommended

#### Software Requirements

* Arduino IDE or PlatformIO
* ESP32 board support package
* Required ESP32 libraries
* MQTT client library
* Sensor library appropriate for the selected sensor
* Serial terminal/serial monitor
* Git
* GitHub repository
* MQTT client/testing tool such as MQTT Explorer or an equivalent tool
* MQTT broker
* Wi-Fi network with internet or local network access as required by the project

#### Topics

* ESP32
* Wi-Fi
* MQTT
* Sensor data
* Publish/subscribe architecture
* Network communication
* Message handling

#### Completion Criteria

The project is complete when:

1. The ESP32 successfully connects to the configured Wi-Fi network.
2. The ESP32 successfully connects to the MQTT broker.
3. The device publishes sensor data successfully.
4. At least **20 MQTT messages** are published and verified.
5. The device successfully subscribes to at least **1 MQTT topic**.
6. At least **10 received MQTT commands/messages** are processed correctly.
7. Wi-Fi disconnection behavior is tested.
8. MQTT disconnection or broker failure behavior is tested.
9. The system recovers from at least **1 simulated communication failure**.
10. MQTT topics and message formats are documented.
11. At least **1 networking or communication problem** is investigated and resolved.
12. The project can be rebuilt and demonstrated using the README instructions.

---

## Common Software Requirements

For every project:

* Use a documented compiler/toolchain.
* Record the software versions used.
* Keep source code under Git version control.
* Document project dependencies.
* Document build and upload/flash procedures.
* Keep generated build files out of the repository.
* Do not commit passwords, API keys, Wi-Fi credentials, MQTT credentials, or other secrets.
* Use a serial terminal when serial debugging is required.
* Keep the README sufficient for another person to reproduce the software setup.

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
