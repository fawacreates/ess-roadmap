# Phase 5 — Real-Time Operating Systems

Projects focused on understanding how embedded applications move from simple super-loop programs into structured real-time systems.

## Projects

### 1. Multi-Task LED System

Status: Not Started

#### Architecture

```text
                    STM32 MCU
                        |
                 FreeRTOS Scheduler
                        |
        +---------------+---------------+
        |               |               |
        v               v               v
   LED Task 1       LED Task 2       LED Task 3
        |               |               |
        v               v               v
     LED 1            LED 2            LED 3
```

Task flow:

```text
Task Creation
      |
      v
FreeRTOS Scheduler
      |
      +----> LED Task 1 ----> Delay ----+
      |                                |
      +----> LED Task 2 ----> Delay ----+----> Scheduler
      |                                |
      +----> LED Task 3 ----> Delay ----+
```

The architecture demonstrates multiple independent tasks running under the FreeRTOS scheduler.

#### Hardware Requirements

* STM32 development board
* LEDs
* Appropriate current-limiting resistors
* Breadboard
* Jumper wires
* USB cable
* Computer
* Logic analyzer — optional
* Multimeter — recommended

#### Software Requirements

* STM32CubeIDE
* STM32CubeMX — included with or integrated into the STM32 development workflow
* FreeRTOS
* STM32 HAL/CMSIS libraries
* C compiler/toolchain provided by STM32CubeIDE
* Serial terminal — if serial debugging is used
* Git
* GitHub repository

#### Topics

* FreeRTOS
* Tasks
* Task creation
* Task states
* Task scheduling
* Task priorities
* Delays
* Periodic tasks
* Context switching
* State machines

#### Completion Criteria

The project is complete when:

1. FreeRTOS starts successfully on the target microcontroller.
2. At least **3 independent tasks** are implemented.
3. Each task performs a clearly defined function.
4. Task priorities are documented.
5. The behavior of each task is verified independently.
6. At least **3 different scheduling scenarios** are tested.
7. LED timing remains correct during concurrent task execution.
8. At least **1 scheduling or timing problem** is investigated and resolved.
9. Task states and important scheduling behavior are documented.
10. The project can be rebuilt and demonstrated using the README instructions.

---

### 2. Sensor → Queue → Processing → UART Architecture

Status: Not Started

#### Architecture

```text
                    STM32 MCU
                        |
                 FreeRTOS Scheduler
                        |
        +---------------+----------------+
        |                                |
        v                                v
 Sensor Acquisition Task            Processing Task
        |                                ^
        |                                |
        v                                |
   Sensor Data -----------------> FreeRTOS Queue
                                         |
                                         v
                                  Processed Data
                                         |
                                         v
                                  UART Output Task
                                         |
                                         v
                                  Serial Terminal
```

Data flow:

```text
Sensor
  |
  v
Sensor Acquisition Task
  |
  v
FreeRTOS Queue
  |
  v
Processing Task
  |
  v
Processed Result
  |
  v
UART
  |
  v
PC / Serial Terminal
```

The architecture demonstrates a producer-consumer model where one task produces sensor data and another task consumes and processes it.

#### Hardware Requirements

* STM32 development board
* Sensor compatible with the selected interface
* Breadboard
* Jumper wires
* USB cable
* Computer
* Logic analyzer — optional
* Multimeter — recommended

#### Software Requirements

* STM32CubeIDE
* STM32CubeMX — included with or integrated into the STM32 development workflow
* FreeRTOS
* STM32 HAL/CMSIS libraries
* C compiler/toolchain provided by STM32CubeIDE
* Serial terminal
* Git
* GitHub repository

#### Topics

* FreeRTOS tasks
* Queues
* Producer-consumer architecture
* Inter-task communication
* Task scheduling
* UART
* Sensor acquisition
* Data processing
* Buffering
* Task priorities

#### Completion Criteria

The project is complete when:

1. A dedicated task successfully acquires sensor data.
2. Sensor data is transferred through a FreeRTOS queue.
3. A separate processing task receives and processes the queued data.
4. A UART task or output mechanism reports the processed results.
5. At least **20 sensor data samples** successfully travel through the complete pipeline.
6. Queue behavior is tested under both normal and increased data-production conditions.
7. Queue-full behavior is tested and documented.
8. At least **3 different sensor conditions or input values** are processed.
9. At least **1 inter-task communication problem** is investigated and resolved.
10. Task responsibilities and data flow are documented.
11. Task priorities and queue configuration are documented.
12. The project can be rebuilt and demonstrated using the README instructions.

---

### 3. Multi-Task Environmental Monitoring System

Status: Not Started

#### Architecture

```text
                         STM32 MCU
                             |
                      FreeRTOS Scheduler
                             |
       +----------+----------+----------+----------+
       |          |                     |          |
       v          v                     v          v
 Sensor Task  Processing Task      Communication  Monitor/
       |          |                     Task       Control
       |          |                       |          Task
       v          v                       v          v
 Temperature   Data Processing         UART /      System
 Humidity      Filtering              Display      Status
 Sensor        Validation             Output
       |          |
       +----------+
             |
             v
      Shared System Data
             |
      +------+------+
      |             |
      v             v
   Queue/Buffer   Synchronization
```

A simplified system flow:

```text
Sensors
   |
   v
Sensor Acquisition
   |
   v
Data Queue / Buffer
   |
   v
Processing
   |
   +--------------------+
   |                    |
   v                    v
Display / UART      System State
                        |
                        v
                  Monitoring Task
```

Possible synchronization structure:

```text
Task A --------+
               |
Task B --------+----> Shared Resource
               |          |
Task C --------+          v
                       Mutex
                          |
                          v
                   Protected Access
```

The architecture demonstrates a multi-task embedded system where sensor acquisition, processing, communication, and system monitoring operate concurrently.

#### Hardware Requirements

* STM32 development board
* Temperature/humidity sensor
* Additional sensor or input device
* Display or UART output
* Breadboard
* Jumper wires
* USB cable
* Computer
* Logic analyzer — optional
* Multimeter — recommended

#### Software Requirements

* STM32CubeIDE
* STM32CubeMX — included with or integrated into the STM32 development workflow
* FreeRTOS
* STM32 HAL/CMSIS libraries
* C compiler/toolchain provided by STM32CubeIDE
* Serial terminal
* Git
* GitHub repository

#### Topics

* Multiple FreeRTOS tasks
* Task scheduling
* Queues
* Semaphores
* Mutexes
* Task notifications
* Software timers
* Event groups
* Stream buffers
* Message buffers
* State machines
* Resource sharing
* Error handling

#### Completion Criteria

The project is complete when:

1. At least **4 independent tasks** are implemented.
2. Each task has a clearly documented responsibility.
3. Sensor acquisition and processing occur concurrently.
4. Inter-task communication is implemented using appropriate FreeRTOS mechanisms.
5. At least **2 different synchronization mechanisms** are used where appropriate.
6. Shared resources are protected against unsafe concurrent access.
7. At least **3 concurrency-related test scenarios** are completed.
8. At least **20 environmental measurements** are successfully processed.
9. Task priorities are documented and justified.
10. At least **1 race-condition, synchronization, timing, or scheduling problem** is investigated and resolved.
11. Relevant task/resource usage is evaluated.
12. The system demonstrates predictable behavior during concurrent operation.
13. The project can be rebuilt and demonstrated using the README instructions.

---

## Architecture Documentation Requirements

Every RTOS project should include an architecture diagram showing:

* Microcontroller
* FreeRTOS scheduler
* Tasks
* Task responsibilities
* Queues and buffers
* Synchronization mechanisms
* Hardware interfaces
* Data flow
* Communication paths
* Shared resources where applicable

The architecture diagram should be updated if the implementation changes significantly.

Recommended diagram progression:

```text
Initial Design
      |
      v
Implementation
      |
      v
Debugging
      |
      v
Final Architecture
```

The final architecture diagram should represent the actual implemented system rather than only the original design.

## Common Hardware and Documentation Requirements

For every RTOS hardware project:

* Document the exact development board used.
* Document the exact sensors, LEDs, displays, and modules used.
* Document operating voltages.
* Document wiring and pin connections.
* Include a circuit diagram where useful.
* Include relevant datasheets.
* Record important hardware configuration details.
* Include photographs of the completed hardware setup where useful.
* Verify voltage and pin requirements before connecting hardware.

## Common Software Requirements

For every RTOS project:

* Use a documented compiler/toolchain.
* Record the software versions used.
* Document the FreeRTOS version used.
* Document the target microcontroller.
* Keep source code under Git version control.
* Document project dependencies.
* Document build and flash procedures.
* Keep generated build files out of the repository.
* Do not commit passwords, API keys, or other secrets.
* Document RTOS configuration.
* Document task priorities and important timing parameters.
* Keep the README sufficient for another person to reproduce the software setup.

## RTOS Documentation Requirements

Every RTOS project should document:

* Task architecture
* Task responsibilities
* Task priorities
* Task states where relevant
* Inter-task communication
* Synchronization mechanisms
* Shared resources
* Timing requirements
* Queue/buffer configuration
* Important scheduling decisions
* Problems encountered
* Debugging process
* Resource considerations
* Testing results

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
