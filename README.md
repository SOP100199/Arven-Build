# ARVEN

ARVEN is an experimental processor architecture project developed from first principles.

The project aims to explore the complete lifecycle of a custom CPU:

- Instruction Set Architecture (ISA)
- Assembly language
- Assembler
- CPU simulator
- Debugger
- RTL implementation
- FPGA implementation
- Embedded peripherals
- Future Edge-AI extensions

## Current Architecture

### ARVEN-16 v0.1

| Component | Specification |
|---|---|
| ISA Style | Hybrid RISC |
| Data Width | 16-bit |
| General Registers | 8 × 16-bit |
| Address Width | 16-bit |
| Address Space | 64 KB |
| Memory Model | Load/Store |
| Endianness | Little-endian |
| Base Instruction Size | 16-bit |
| Extended Instruction Size | 32-bit |
| Addressing Modes | Register, Immediate, Absolute, Indirect, Offset, PC-relative |
| Branching | PC-relative |
| Flags | Z, C, N, V |
| Stack | Dedicated Stack Pointer |
| AI | Future ISA extension |

## Status

ARVEN is currently in the architecture and ISA design phase.

The repository is an experimental development workspace. The finalized architecture will eventually be published as a separate official repository.