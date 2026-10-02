# Measurable Pass or Fail Thresholds

A project is marked **PASS** only when it meets the required thresholds below. If any mandatory threshold is not met, the project remains **FAIL / Incomplete** until the issue is resolved.

## Universal Pass Criteria

### 1. Requirements

**PASS**

* Project objective is documented.
* Expected inputs and outputs are documented.
* Required hardware and software are documented.
* Success criteria are defined before final testing.

**FAIL**

* Objective is unclear.
* Required inputs or outputs are unknown.
* Project cannot be reproduced from the documented requirements.

---

### 2. Core Functionality

**PASS**

* At least **100% of the defined core requirements** work as intended.
* No known critical functionality is broken.
* The project can be demonstrated successfully at least **3 consecutive times** under the documented normal conditions.

**FAIL**

* Any core requirement does not work.
* The project only works intermittently without an understood reason.
* The project cannot be reproduced reliably.

---

### 3. Testing

**PASS**

* At least **5 meaningful test cases** are documented for a small project.
* At least **10 meaningful test cases** are documented for a medium or advanced project.
* All critical test cases pass.
* At least **1 edge case** is tested.
* At least **1 error condition** is tested where applicable.

**FAIL**

* Testing consists only of one successful run.
* Critical test cases fail.
* Test results are not recorded.

---

### 4. Debugging

**PASS**

* At least **1 real bug or technical problem** is investigated.
* Root cause is identified.
* Fix is implemented.
* Fix is verified with a repeat test.
* Debugging process is documented.

**FAIL**

* No meaningful debugging was performed when the project had an opportunity for it.
* The problem was fixed without understanding the cause.
* The fix was not verified.

---

### 5. Documentation

**PASS**
The README contains at minimum:

1. Objective
2. Requirements
3. Setup instructions
4. Build/run instructions
5. Usage
6. Implementation overview
7. Testing results
8. Debugging notes
9. Problems and solutions
10. What was learned
11. Limitations
12. Future improvements

**FAIL**

* Essential setup or usage information is missing.
* Another person cannot reasonably reproduce the project from the documentation.

---

### 6. Git

**PASS**

* Project is committed to Git.
* At least **3 meaningful commits** exist for a small project.
* At least **5 meaningful commits** exist for a medium/advanced project.
* Commit messages describe the actual changes.
* No passwords, API keys, or other secrets are committed.
* No unnecessary build artifacts are committed.

**FAIL**

* Only one final dump commit exists when meaningful development history should exist.
* Secrets are committed.
* Repository contains unnecessary generated files that should be ignored.

---

## Phase-Specific Pass Criteria

### Phase 1 — C Programming

**PASS**

* Required C concepts are demonstrated in working code.
* At least **5 test cases** are executed for small projects.
* Dynamic-memory projects show correct allocation and deallocation.
* No known memory leak remains in the tested execution paths.
* Compiler warnings are reduced to **zero warnings** using the selected warning configuration, or every remaining warning is documented and justified.
* Code can be built from a clean environment using the documented instructions.

**FAIL**

* Core C concepts are only copied from a tutorial without modification or understanding.
* Memory leaks or invalid memory access remain unresolved.
* Important compiler warnings remain unexplained.
* Project cannot be rebuilt from the documentation.

---

### Phase 2 — Computer Architecture and OS Basics

**PASS**

* Required architecture concepts are correctly explained.
* At least **3 concrete observations** are documented for analysis-based projects.
* C-to-assembly analysis identifies the relevant instructions, registers, or stack behavior.
* Endianness programs produce correct results for at least **3 different test values**.
* Technical notes explain the complete execution path being studied.

**FAIL**

* Results are presented without explanation.
* Important architectural behavior is misunderstood.
* Analysis cannot be reproduced.

---

### Phase 3 — Microcontrollers and Bare-Metal Programming

**PASS**

* Firmware runs successfully on the target microcontroller.
* Required peripherals operate correctly.
* Hardware behavior is verified through measurements, serial output, debugger output, or another appropriate method.
* At least **3 successful hardware test runs** are completed.
* At least **1 fault or incorrect behavior** is intentionally or naturally investigated.
* Relevant datasheet/reference-manual information is documented.
* Firmware can be rebuilt from a clean environment.

**FAIL**

* Firmware only works in simulation when actual hardware is required.
* Hardware behavior is not verified.
* Peripheral configuration is undocumented.
* The system works only once and cannot be reproduced.

---

### Phase 4 — Communication Protocols

**PASS**

* At least **20 valid communication transactions** are tested.
* At least **5 invalid/error transactions** are tested where applicable.
* Communication errors are detected correctly.
* CRC/error checking works when required by the project.
* Timing or protocol behavior is verified using appropriate tools where applicable.
* Lost, corrupted, or malformed data is handled according to the project design.

**FAIL**

* Only successful communication is tested.
* Invalid data causes undefined behavior.
* Communication failures are not detected or documented.

---

### Phase 5 — RTOS

**PASS**

* All required tasks execute correctly.
* Inter-task communication is demonstrated.
* Synchronization mechanisms behave correctly.
* At least **3 concurrency-related test scenarios** are tested.
* No unresolved race condition or deadlock is known.
* Task priorities and major scheduling decisions are documented.
* Relevant stack/resource usage is evaluated.

**FAIL**

* Tasks communicate through unsafe shared state without justification.
* Deadlocks or race conditions remain unresolved.
* Task behavior cannot be reproduced reliably.

---

### Phase 6 — Electronics

**PASS**

* Circuit matches the documented schematic.
* At least **3 meaningful measurements** are recorded for measurement-based projects.
* Measured values are within the project's defined acceptable tolerance.
* Relevant component datasheets are consulted.
* Expected and measured behavior are compared.
* Hardware faults or unexpected behavior are documented and investigated.

**FAIL**

* Circuit behavior is accepted without measurement when measurement is required.
* Critical electrical values are outside the defined limits.
* Component specifications are ignored.
* Hardware cannot be reproduced from the documentation.

---

### Phase 7 — Embedded Linux and Professional Practices

**PASS**

* Target system boots successfully.
* Application builds using the documented toolchain.
* Application runs successfully on the target.
* At least **5 functional test cases** are completed.
* Debugging tools are used where appropriate.
* Build and deployment steps are reproducible.
* Relevant static analysis or testing results are documented.

**FAIL**

* Application only works on the development machine.
* Target build cannot be reproduced.
* Deployment procedure is undocumented.
* Critical test cases fail.

---

### Phase 8 — Specialization and Job Readiness

**PASS**

* Project combines multiple previously learned embedded concepts.
* At least **10 meaningful test cases** are documented.
* At least **2 real technical problems** are investigated and documented.
* System architecture is documented.
* Hardware/software interfaces are documented.
* Testing and debugging evidence is included.
* A new person can understand the project from the README without requiring undocumented information.
* Project can be demonstrated from a clean setup.

**FAIL**

* Project is primarily a tutorial reproduction.
* Major design decisions cannot be explained.
* Testing evidence is missing.
* Project cannot be reproduced or demonstrated from the documentation.

---

# Final PASS / FAIL Rule

A project receives:

**PASS**
when:

1. All mandatory universal criteria are satisfied.
2. All mandatory phase-specific criteria are satisfied.
3. All critical functionality passes.
4. No unresolved critical bug remains.
5. Documentation is sufficient for reproduction.

**FAIL / INCOMPLETE**
when:

1. Any mandatory criterion is not satisfied.
2. Any critical functionality fails.
3. A reproducibility problem remains.
4. A critical bug remains unresolved.
5. Required testing or documentation is missing.

## Status Levels

Use the following status values in the repository:

```text
NOT STARTED
    ↓
IN PROGRESS
    ↓
TESTING
    ↓
PASS
```

If a project does not meet the required threshold:

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

A project should never be marked **PASS** simply because the main demonstration works once.
