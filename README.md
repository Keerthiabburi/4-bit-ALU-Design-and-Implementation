# 4-bit ALU Design and Implementation

## 📘 Project Concept

The Arithmetic and Logic Unit (ALU) is a central component in digital processors, responsible for executing arithmetic and logic operations. This project involves designing a **4-bit ALU** capable of performing the following operations:
- **Addition**
- **Subtraction**
- **Bitwise XOR**
- **Bitwise NOT**

The ALU uses a **Ripple-Carry Adder (RCA)** for arithmetic operations and basic combinational logic for logical functions. A **multiplexer-based selector** chooses the correct output based on a 2-bit control signal.

The objective was to realize this design both in **behavioral form (RTL)** and **physical form (transistor-level)** to bridge high-level abstraction with low-level circuit implementation — a key learning goal in VLSI design.

---

## 🛠 Tools & Technologies

- **Verilog HDL** – RTL modeling of ALU
- **Xilinx Vivado 2020.1** – Simulation and functional verification
- **Cadence Virtuoso** – CMOS gate-level schematic and transient simulation
- **Power Analyzer, Timing Analyzer** – For area, delay, and power evaluation

---

## ⚙️ ALU Architecture

- **Inputs**: 2 × 4-bit binary operands (`A`, `B`) and a 2-bit control signal
- **Control Logic**: Selects one of four operations using a 4:1 multiplexer
- **Arithmetic Unit**: 4-bit Ripple-Carry Adder for ADD/SUB (with 2's complement)
- **Logic Unit**: Bitwise XOR and NOT using CMOS logic gates
- **Output**: 4-bit result + optional carry-out (for addition)

---

## ✅ Functional Implementation

### RTL Design (Verilog)
- Developed full Verilog modules: Full Adder, RCA, 2:1 and 4:1 MUX, ALU logic
- Simulated using Vivado Testbenches
- Verified correct results for all ALU operations

### Transistor-Level Design (CMOS)
- Designed Full Adder, XOR gate, NOT gate, and MUX using CMOS logic
- Constructed a full 4-bit ALU schematic in Cadence Virtuoso
- Performed transient analysis to verify logical correctness and measure:
  - **Propagation Delay**
  - **Power Consumption**
  - **Area Utilization**

---

## 📊 Comparative Summary

| Aspect            | RTL (Vivado)              | CMOS (Cadence Virtuoso)         |
|------------------|----------------------------|----------------------------------|
| Abstraction       | Behavioral model           | Transistor-level physical design |
| Simulation        | Functional testbenches     | Transient waveform analysis      |
| Design Focus      | Correct logic behavior     | Real-world constraints (delay, power) |
| Use Case          | FPGA or digital synthesis  | ASIC or full-custom VLSI         |

---

## 🚀 Future Extensions
- Add more operations (AND, OR, NAND, NOR, Shift)
- Extend ALU to 8 or 16 bits
- Implement pipelining for performance
- Explore layout-level design and DRC/LVS checks

---

## 👥 Contributors

- Abburi Sai Keerthi – BL.EN.U4ECE22002  
- B. Asritha Venkata Naga Hasini – BL.EN.U4ECE22010  
- Bommisetty Lakshmi Sowmya – BL.EN.U4ECE22011  
- Megha Elango – BL.EN.U4ECE22035  

**Faculty In-charge**: Mr. Vignesh, Mr. Swaminadhan  
**Institution**: Amrita School of Engineering  
**Academic Year**: 2024–2025 (Even Semester)

---

📝 *This project reflects a full-stack digital design workflow from RTL coding to transistor-level schematic design and analysis, essential for careers in VLSI, embedded systems, and digital hardware design.*
