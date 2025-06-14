# RISCV32
This project implements a 32-bit RISC-V processor core using Verilog. It supports the RV32I base instruction set, including fetch, decode, execute, memory, and writeback stages. Designed for FPGA deployment, simulation, and educational CPU architecture study.
# 32-bit RISC-V Processor Core (RV32I)

This project is a Verilog-based implementation of a 32-bit RISC-V processor core conforming to the RV32I instruction set architecture (ISA). Designed for educational use, simulation, and FPGA deployment, the processor features a modular and extensible architecture.

---

## 🔧 Features

- ✅ **Supports RV32I Base Integer Instruction Set**
- ⚙️ **Five-Stage Pipeline (optional: Single-Cycle or Multi-Cycle)**
  - Instruction Fetch (IF)
  - Instruction Decode (ID)
  - Execute (EX)
  - Memory Access (MEM)
  - Write Back (WB)
- 📦 **Modular Design for Easy Extension**
- 🧪 **Includes Testbenches and Simulation Support**
- 🖥️ **FPGA-Friendly Design**
- 📁 **Instruction and Data Memory Integration**

---

## 📁 Repository Structure

```bash
RISC-V32/
│
├── src/                   # All Verilog modules
│   ├── alu.v
│   ├── control_unit.v
│   ├── datapath.v
│   ├── register_file.v
│   └── riscv_core.v
│
├── testbench/             # Testbenches and sample programs
│   ├── tb_top.v
│   ├── memory_model.v
│   └── sample_programs/
│
├── docs/                  # Documentation and diagrams
│   ├── architecture.png
│   └── instruction_set.md
│
├── fpga/                  # FPGA constraints and synthesis files
│   ├── constraints.xdc
│   └── riscv_top.v
│
└── README.md              # Project overview
🚀 Getting Started
Requirements
Verilog simulator (e.g., ModelSim, Icarus Verilog)

GTKWave (for waveform visualization)

(Optional) FPGA Toolchain (Vivado, Quartus, etc.)

Simulation
bash
Copy
Edit
# Using Icarus Verilog
cd testbench
iverilog -o riscv_tb tb_top.v ../src/*.v
vvp riscv_tb
gtkwave dump.vcd
FPGA Deployment
Open the fpga/ directory in your preferred FPGA tool.

Use the provided riscv_top.v and constraints.xdc (Xilinx) or .qsf (Intel).

Synthesize, implement, and program your FPGA board.

📜 Instruction Set Support
Category	Instructions
Arithmetic	ADD, SUB, SLT, SLTU
Logical	AND, OR, XOR, SLL, SRL
Control Flow	BEQ, BNE, JAL, JALR
Memory Access	LW, SW
Immediate Ops	ADDI, ANDI, ORI, etc.

📚 Documentation
Detailed architecture diagrams are available in the docs/ folder.

Instruction Set documentation: docs/instruction_set.md

💡 Future Work
 Add RV32M (Multiply/Divide) Extension

 Support for CSR and Exceptions

 Cache Memory Integration

 Linux Bootable SoC Platform

👨‍💻 Contributors
Manohar KM – Developer & Verilog Engineer

Srinivasamurthy Sir – Supervisor, Associate Professor
