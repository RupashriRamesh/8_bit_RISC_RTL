# 8-bit RISC Processor in Verilog RTL

A single-cycle 8-bit RISC processor implemented using Verilog RTL, simulated in ModelSim, and synthesizable in Quartus Prime.

---

## 📌 Project Overview

This project implements an 8-bit RISC processor based on a **single-cycle architecture**, where each instruction completes fetch, decode, execute, and write-back in **one clock cycle**.

The processor demonstrates a simplified RISC instruction set supporting **arithmetic, logic, comparison, shift, move, jump, and halt operations**.

---

## ⚙️ Features

- **Single-Cycle Architecture** – One instruction per clock cycle  
- **16×16-bit ROM** – Stores program instructions  
- **16×8-bit RAM** – Handles data storage  
- **16 General Purpose Registers** – 8-bit wide each  
- **ALU Implementation** – Supports arithmetic and logical operations  
- **Control Unit** – Decodes instructions and manages data flow  
- **Jump & Halt Support** – Implements program flow control  
- **Waveform Verification** – Functional simulation in ModelSim  

---

## 🏗️ Project Structure

```RISC-Processor/
├── docs/  # Documentation & reports
│ ├── RISC_Report.pdf
│ ├── RTL_View.pdf
│ ├── Waveform.png
│ └── Transcript.png
├── src/ # Verilog HDL source files
│ ├── RISC_Top_Module.v
│ ├── ALU.v
│ ├── Control_Unit.v
│ ├── Register_File.v
│ ├── RAM.v
│ ├── ROM.v
│ ├── MUX.v
│ └── RISC_TB.v # Testbench
├── simulations/ # Simulation outputs
│ ├── waveform.bmp
│ └── simulation_transcript.txt
│ └── RTL_Viewer
├── quartus/ # Quartus project files
│ └── RISC.qpf
├── .gitignore
├── README.md
└── LICENSE
```


---

## 🧩 Instruction Set Architecture (ISA)

| Opcode | Instruction | Operation | Description |
|--------|------------|-----------|-------------|
| 0000   | ADD        | R[rd] = R[rs1] + R[rs2] | Addition |
| 0001   | SUB        | R[rd] = R[rs1] - R[rs2] | Subtraction |
| 0010   | AND        | R[rd] = R[rs1] & R[rs2] | Bitwise AND |
| 0011   | OR         | R[rd] = R[rs1] \| R[rs2] | Bitwise OR |
| 0100   | XOR        | R[rd] = R[rs1] ^ R[rs2] | Bitwise XOR |
| 0101   | CMP        | Flags = Compare(Rs1,Rs2) | Comparison |
| 0110   | SHL        | R[rd] = R[rs1] << 1 | Logical Shift Left |
| 0111   | SHR        | R[rd] = R[rs1] >> 1 | Logical Shift Right |
| 1000   | MOV        | R[rd] = R[rs1] | Move Register |
| 1001   | JMP        | PC = Immediate Address | Jump |
| 1111   | HLT        | Stop Execution | Halt |

---

## 🧪 Simulation & Results

- **Simulation Tool:** ModelSim  
- **Verification:** Testbench verifies all supported instructions  

**Outputs:**

- Waveform showing instruction execution  
- Transcript showing register updates  
- RTL Viewer showing synthesized hardware blocks  

---

## 🛠️ Tools & Technologies

- **HDL:** Verilog RTL  
- **Simulation:** ModelSim  
- **Synthesis:** Quartus Prime  
- **Target:** FPGA-ready design  

---

## 📄 How to Run

1. Clone the repository:  
```bash
git clone https://github.com/RupashriRamesh/8_bit_RISC_RTL.git 
```
2. Open ModelSim.
3. Compile all .v files from the src/ folder.
4. Load the RISC_TB testbench.
5. Run the simulation and view the waveform.

📚 Documentation

Detailed explanation of architecture, instruction set, and simulation results is available in [RISC_Processor_Report.pdf](docs/Risc_Processor_report.pdf).


### 📌 Future Enhancements

- Multi-cycle architecture implementation  
- Pipeline execution support  
- Integration with FPGA hardware  
- Enhanced instruction set

📜 License

This project is licensed under the MIT License.

✍️ Author
Rupashri R