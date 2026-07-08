
# Direct CXL Memory to LPDDR5X Controller Bridge for Edge-AI Supernodes

> RTL Design | Computer Architecture | Memory Systems | CXL | LPDDR5X | Edge AI

## Overview

Modern Edge-AI applications demand high memory bandwidth and low-latency access while supporting increasingly larger AI models. Compute Express Link (CXL) has emerged as a next-generation coherent interconnect for memory expansion, whereas LPDDR5X provides high-performance, low-power memory suitable for edge computing platforms.

This project proposes an RTL-based **Direct CXL Memory to LPDDR5X Controller Bridge** that enables seamless communication between a CXL.mem interface and an LPDDR5X memory controller. The bridge is designed to efficiently translate CXL memory transactions into LPDDR5X memory commands while minimizing latency and maximizing memory throughput for Edge-AI Supernodes.

---

## Project Objectives

- Design an RTL-based CXL-to-LPDDR5X Bridge.
- Implement CXL.mem request handling.
- Develop address translation and transaction management.
- Interface with an LPDDR5X Memory Controller.
- Evaluate latency, throughput, and bandwidth.
- Explore architectural optimizations for Edge-AI memory systems.

---

## System Architecture

```
                +----------------------+
                |    Host / CPU / NPU  |
                +----------+-----------+
                           |
                    CXL.mem Interface
                           |
                +----------v-----------+
                |   CXL Root Complex   |
                +----------+-----------+
                           |
                +----------v-----------+
                |   CXL-LPDDR5X Bridge |
                |                      |
                | • Address Translation|
                | • Request Scheduler  |
                | • Transaction Buffer |
                +----------+-----------+
                           |
                +----------v-----------+
                | LPDDR5X Controller   |
                +----------+-----------+
                           |
                     LPDDR5X Memory
```

---

## Project Workflow

```
CXL Request
      │
      ▼
Packet Decoder
      │
      ▼
Address Translation
      │
      ▼
Transaction Scheduler
      │
      ▼
LPDDR5X Command Generator
      │
      ▼
Memory Controller
      │
      ▼
LPDDR5X DRAM
```

---

## Design Modules

### CXL Interface
- CXL.mem transaction handling
- Packet decoding
- Request generation

### Bridge Logic
- Address translation
- Read/Write arbitration
- Buffer management
- Transaction scheduling

### LPDDR5X Controller
- ACT
- PRE
- READ
- WRITE
- REFRESH
- Timing management

### Verification
- Functional simulation
- RTL verification
- Timing verification
- Performance evaluation

---

## Development Flow

```
Architecture Design
        │
        ▼
RTL Design (Verilog/SystemVerilog)
        │
        ▼
Functional Verification
        │
        ▼
Synthesis
        │
        ▼
Static Timing Analysis
        │
        ▼
Performance Evaluation
```

## Reference Papers

### Primary Reference

**CXL-GPU: Pushing GPU Memory Boundaries with the Integration of CXL Technologies**

IEEE Micro, 2025

Key Concepts:
- CXL Root Complex
- CXL Controller
- Host Bridge
- CXL.mem Architecture
- RTL Implementation

---

### Supporting Reference

**Ramulator 2.0: A Modern, Modular and Extensible DRAM Simulator**

IEEE Computer Architecture Letters, 2024

Key Concepts:
- LPDDR5 Memory Model
- DRAM Scheduling
- Memory Controller
- Timing Constraints
- Performance Evaluation

---


## Author

**SARATH K C**


## License

This repository is intended for academic and research purposes.
