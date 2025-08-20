🖥️ 8-bit RISC Processor in Verilog
A single-cycle 8-bit RISC processor implemented using Verilog HDL, simulated in ModelSim and synthesizable in Quartus Prime.

📌 Project Overview

This project implements an 8-bit RISC processor based on a single-cycle architecture, where each instruction completes its fetch, decode, execute, and write-back stages within one clock cycle.

The processor is designed and simulated using Verilog HDL and ModelSim. It demonstrates a simplified RISC instruction set supporting arithmetic, logic, comparison, shift, move, jump, and halt operations.


⚙️ Features

Single-Cycle Architecture – One instruction per clock cycle
16×16-bit ROM – Stores program instructions
16×8-bit RAM – Handles data storage
16 General Purpose Registers – 8-bit wide each
ALU Implementation – Supports arithmetic and logical operations
Control Unit – Decodes instructions and manages data flow
Jump & Halt Support – Implements program flow control
Waveform Verification – Functional simulation in ModelSim


🏗️ Project Structure

RISC-Processor/
│
├── 📂 docs/                # Documentation & reports
│   ├── RISC_Report.pdf      # Detailed project report
│   ├── RTL_View.pdf         # RTL schematic diagram
│   ├── Waveform.png         # Simulation waveform image
│   ├── Transcript.png       # ModelSim simulation transcript
│
├── 📂 src/                 # Source files (Verilog HDL)
│   ├── RISC_Top_Module.v    # Top-level processor module
│   ├── ALU.v                # Arithmetic & Logic Unit
│   ├── Control_Unit.v       # Instruction decoder
│   ├── Register_File.v      # 16x8 register implementation
│   ├── RAM.v                # Data memory
│   ├── ROM.v                # Instruction memory
│   ├── MUX.v                # Multiplexers used in design
│   ├── RISC_TB.v            # Testbench for simulation
│
├── 📂 simulations/          # Simulation outputs
│   ├── waveform.bmp         # Captured waveform
│   ├── simulation_transcript.txt       # ModelSim console log
│
├── 📂 quartus/             
│   ├── RISC.qpf             # Quartus Project File
│      
├── .gitignore
├── README.md
└── LICENSE 


🧩 Instruction Set Architecture (ISA)

Opcode	 Instruction	Operation	         Description

0000	   ADD	       R[rd] = R[rs1] + R[rs2]	  Addition
0001	   SUB	       R[rd] = R[rs1] - R[rs2]	  Subtraction
0010	   AND	       R[rd] = R[rs1] & R[rs2]	  Bitwise AND
0011	   OR	       R[rd] = R[rs1] |	R[rs2]    Bitwise OR
0100	   XOR	       R[rd] = R[rs1] ^ R[rs2]	  Bitwise XOR
0101	   CMP	       Flags = Compare(Rs1,Rs2)	  Comparison
0110	   SHL	       R[rd] = R[rs1] << 1	  Logical Shift Left
0111	   SHR	       R[rd] = R[rs1] >> 1	  Logical Shift Right
1000	   MOV	       R[rd] = R[rs1]	          Move Register
1001	   JMP	       PC = Immediate Address	  Jump
1111	   HLT	       Stop Execution	          Halt Instruction

You can include a waveform snippet in the report instead of here.


🧪 Simulation & Results

Simulation Tool: ModelSim
Verification: Testbench verifies all supported instructions

Outputs:

Waveform showing instruction execution
Transcript showing register updates
RTL Viewer showing synthesized hardware blocks


🛠️ Tools & Technologies

Hardware Description Language: Verilog HDL
Simulation Tool: ModelSim
Synthesis Tool: Quartus Prime 
Target Device: FPGA-ready design 


📄 How to Run

Clone the repository: git clone https://github.com/YourUsername/RISC-Processor.git
Open ModelSim.
Compile all .v files from the src/ folder.
Load the RISC_TB testbench.
Run the simulation and view the waveform.


📚 Documentation

Detailed explanation of architecture, instruction set, and simulation results is available in: RISC_Report.pdf


📌 Future Enhancements

Multi-cycle architecture implementation
Pipeline execution support
Integration with FPGA hardware
Enhanced instruction set

📜 License This project is licensed under the MIT License

✍️ Author
Rupashri Ramesh
