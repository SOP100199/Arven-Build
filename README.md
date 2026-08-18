# ARVEN

**ARVEN** is an open experimental processor architecture designed for
deterministic real-time embedded computing, with a scalable path toward
specialized Edge-AI acceleration.

The project is being developed from the architectural level downward:

- Processor architecture
- Instruction Set Architecture (ISA)
- Assembly language
- Machine-code specification
- Assembler
- CPU simulator
- Debugger
- Verification and testing
- RTL implementation
- FPGA implementation
- Embedded peripherals
- System-on-Chip (SoC) integration
- Future DSP and Edge-AI extensions

---

## Project Status

ARVEN is currently in the **CPU architecture and ISA design phase**.

The initial processor architecture is:

> **ARVEN-16**

The current repository is the experimental development repository:

> `arven-build`

A separate official repository will be created once the architecture,
toolchain, simulator, verification framework, and hardware implementation
reach a sufficiently stable state.

---

# ARVEN-16

ARVEN-16 is the first processor architecture in the ARVEN family.

It is designed around a hybrid RISC philosophy:

- Simple and regular base instructions
- Load/store memory architecture
- Deterministic execution as a design goal
- Compact 16-bit instructions
- 32-bit extended instructions where additional operand space is required
- Architectural extensibility for future specialized instructions

---

## Architectural Baseline

| Component | Specification |
|---|---|
| Architecture | ARVEN-16 |
| ISA Style | Hybrid RISC |
| Data Width | 16-bit |
| Address Width | 16-bit |
| General-Purpose Registers | 8 × 16-bit |
| Address Space | 64 KB |
| Memory Model | Load/Store |
| Memory Addressing | Byte-addressable |
| Endianness | Little-endian |
| Base Instruction Size | 16-bit |
| Extended Instruction Size | 32-bit |
| Branching | PC-relative |
| Status Flags | Z, C, N, V |
| Stack | Dedicated Stack Pointer |
| AI | Future ISA extension |

---

# Design Goals

ARVEN is intended to be more than an educational CPU.

The primary design objective is to create a processor architecture that can
eventually be used in real-time embedded and specialized computing systems.

### Primary goals

- Deterministic execution
- Predictable interrupt behavior
- Simple and efficient instruction decoding
- Hardware implementation suitability
- FPGA compatibility
- Small embedded-system suitability
- Extensible ISA
- Clean software toolchain
- Formal architectural documentation
- Long-term support for specialized accelerators

### Target application areas

- Robotics
- Industrial control
- Embedded instrumentation
- IoT and edge devices
- Motor-control systems
- Sensor-processing systems
- Autonomous embedded systems
- FPGA-based processors
- Specialized real-time controllers
- Future Edge-AI systems

---

# Architecture Philosophy

ARVEN follows several architectural principles.

## 1. Hardware simplicity

The base CPU should remain sufficiently simple to implement,
verify, simulate, and eventually synthesize.

## 2. Deterministic behavior

Real-time applications require predictable system behavior.

Instruction execution, memory access, interrupts, and peripheral interactions
will therefore be designed with determinism as an important architectural
constraint.

## 3. Extensibility

The initial architecture must allow future additions without unnecessarily
breaking existing software.

Potential future extensions include:

- DSP instructions
- Multiply-accumulate operations
- SIMD/vector operations
- Atomic operations
- Specialized AI instructions
- Hardware accelerators

## 4. Software compatibility

The ISA, assembler, simulator, and future hardware implementations should
share a single authoritative architectural specification.

---

# ARVEN Development Roadmap

```text
Architecture
     │
     ▼
ISA Design
     │
     ▼
Instruction Encoding
     │
     ▼
Assembly Language
     │
     ▼
Machine-Code Specification
     │
     ▼
Assembler
     │
     ▼
Simulator
     │
     ▼
Debugger
     │
     ▼
Verification
     │
     ▼
RTL CPU
     │
     ▼
FPGA
     │
     ▼
Real-Time Peripherals
     │
     ▼
ARVEN SoC
     │
     ▼
DSP / Edge-AI Extensions