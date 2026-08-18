# ARVEN-16 Architecture

## 1. Overview

ARVEN-16 is the initial 16-bit processor architecture of the ARVEN project.

The architecture is being designed from first principles with emphasis on:

- Simplicity
- Extensibility
- Educational value
- FPGA implementation
- Software simulation
- Future Edge-AI acceleration

## 2. Architectural Baseline

- ISA style: Hybrid RISC
- Data width: 16-bit
- Address width: 16-bit
- Address space: 64 KB
- General-purpose registers: 8
- Register width: 16-bit
- Memory model: Load/Store
- Endianness: Little-endian
- Base instruction size: 16-bit
- Extended instruction size: 32-bit
- Branching: PC-relative
- Status flags: Z, C, N, V
- Stack: Dedicated SP

## 3. General-Purpose Registers

ARVEN-16 initially provides eight 16-bit general-purpose registers:

R0-R7

Each register is 16 bits wide.

Register identifiers therefore require 3 bits.

## 4. Special Registers

The initial architecture includes:

- PC — Program Counter
- SP — Stack Pointer
- FLAGS — Processor status flags

## 5. Status Flags

ARVEN-16 currently defines four status flags:

- Z — Zero
- C — Carry
- N — Negative
- V — Overflow

The exact behavior of each flag will be formally specified during ISA design.

## 6. Memory

ARVEN-16 uses a 16-bit address space.

Therefore:

2^16 = 65536 bytes = 64 KB

Memory is byte-addressable.

The architecture uses little-endian byte ordering.

## 7. Instruction Encoding

The base instruction size is 16 bits.

32-bit extended instructions are permitted when additional operand or immediate space is required.

Exact instruction formats and opcode assignments are not yet frozen.

## 8. Addressing Modes

The current architectural baseline permits:

- Register
- Immediate
- Absolute
- Register indirect
- Register + offset
- PC-relative

The exact encoding of each addressing mode will be defined in the ISA specification.

## 9. Design Status

This document describes the current architectural baseline.

Instruction formats, opcode assignments, calling conventions, interrupts, privilege levels, and AI extensions remain under design.