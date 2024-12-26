# Nios II Soft Core Processor Overview

## What is Nios II?
Nios II is a widely used 32-bit soft-core processor designed for FPGA applications by Intel (formerly Altera). It offers the flexibility and performance needed for embedded systems, acting as a microcontroller or a system-on-chip (SoC) within programmable logic devices.

---

## Key Features:
### Processor Variants:
- **Fast Core (/f core):**
  - Six-stage pipeline for high performance.
  - Optional Memory Management Unit (MMU) or Memory Protection Unit (MPU).
- **Economy Core (/e core):**
  - One-stage pipeline for minimal size.
  - No license required, making it free to use.
  - Executes one instruction per six clock cycles.

### Architecture:
- Harvard architecture with 32-bit instruction set and data path.
- 32 general-purpose registers with optional shadow register sets for efficient context switching (e.g., interrupts, RTOS).
- Support for up to 32 interrupt sources, extendable via an external interrupt controller.

### Floating Point and Memory:
- Single-precision floating-point operations.
- Address space support for versatile embedded applications.

---

## Development Ecosystem:
- **Platform Designer**: Configures the Nios II processor and its peripherals.
- **Development Tools**:
  - Software development with the GNU C/C++ toolchain.
  - Eclipse IDE integration for project management and debugging.
  
---

## Performance and Use Cases:
- Optimized for use in Intel's FPGAs and available for standard-cell ASICs.
- Access to a wide range of on-chip peripherals and off-chip memory interfaces.
- Commonly implemented in applications requiring flexible, reprogrammable logic such as control systems, signal processing, and embedded operating systems.

---

## Learn More:
- [Nios II Processor Reference Guide](https://www.intel.com/content/dam/www/programmable/us/en/pdfs/literature/hb/nios2/n2cpu-nii5v1gen2.pdf)
- [Nios II Performance Datasheet](https://www.intel.com/content/dam/www/programmable/us/en/pdfs/literature/ds/ds_nios2_perf.pdf)
- [Wikipedia: List of ARM Microarchitectures](https://en.wikipedia.org/wiki/List_of_ARM_microarchitectures)

---

## Hardcore vs Softcore
- Softcore: - Implementation defined by VHDL description
            - Programming of FPGA needed to realize CPU system

- Hardcore: - Implementation defined in silicon
            - CPU system already present in silicon


A soft core processor is a microprocessor fully
described in software, usually in an HDL, which
can be synthesized in programmable
hardware, such as FPGAs

---

## Soft core processor

• Pros:
  - Include the processor core only when needed
  - Include only needed features
  - The number of cores is flexible.
  - Can reuse the design in newer generations of FPGAs in the future. (Mostly vendor limited)

• Cons:
  - May be slower and simpler than hard processor cores.
  - Less area efficient compared to hard cores (Firm IP)