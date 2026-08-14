# 32-bit RISC-V Processor Using Verilog

## Overview

This project implements a simplified 32-bit single-cycle RISC-V processor using Verilog HDL.

The processor implements a subset of the RV32I instruction set and demonstrates the fundamental components of a CPU.

## Supported Instructions

| Instruction | Type | Description |
|---|---|---|
| ADD | R | Add two registers |
| SUB | R | Subtract two registers |
| AND | R | Bitwise AND |
| OR | R | Bitwise OR |
| SLT | R | Set less than |
| ADDI | I | Add immediate |
| LW | I | Load word |
| SW | S | Store word |
| BEQ | B | Branch if equal |

## Architecture

The processor consists of:

- Program Counter
- Instruction Memory
- Control Unit
- Register File
- ALU
- Data Memory
- Immediate Generator
- Branch Logic
- Write-back Logic

## Block Diagram

```text
              +----------------+
              | Program Counter|
              +-------+--------+
                      |
                      v
              +----------------+
              | Instruction    |
              | Memory         |
              +-------+--------+
                      |
                      v
              +----------------+
              | Control Unit   |
              +-------+--------+
                      |
                      v
              +----------------+
              | Register File  |
              +-------+--------+
                      |
                      v
              +----------------+
              |      ALU       |
              +-------+--------+
                      |
             +--------+--------+
             |                 |
             v                 v
       +-------------+   +-------------+
       | Data Memory |   | Write Back  |
       +-------------+   +-------------+