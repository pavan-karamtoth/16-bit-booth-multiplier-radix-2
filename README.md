
# 16-bit Signed Booth Multiplier (Radix-2)

This project implements a **16-bit signed Booth multiplier** using the radix-2 algorithm in **Verilog HDL**.  
The design follows a modular approach with a datapath (adder, shifter, registers) controlled by an **FSM-based control path** to perform efficient two’s-complement multiplication.

## Features
- Supports **signed 16-bit operands** in two’s-complement form  
- Implements the **radix-2 Booth multiplication algorithm**  
- FSM-based control path to sequence operations  
- Iterative datapath with accumulator and arithmetic right-shift  
- Synthesizable on **Xilinx Vivado (FPGA)**  

## File Structure
- `booth_multiplier.v` – Verilog implementation of the radix-2 Booth multiplier  
- `booth_multiplier_tb.v` – Testbench for functional verification  
- `README.md` – Project documentation  

## Simulation & Verification
- Simulated using **Xilinx Vivado**  
- Verified with a wide range of test vectors, including:
  - Zero multiplication (`0 × N`, `N × 0`)  
  - One and negative one (`1 × N`, `-1 × N`)  
  - Maximum positive and minimum negative values (`+32767`, `-32768`)  
  - Positive × Negative combinations  
- Confirmed correctness across all edge cases  

## Results
- Produces correct **32-bit signed product** for all valid input combinations  
- Demonstrates reliable operation in both simulation and synthesis  
- Resource-efficient design suitable for FPGA implementation  

## How to Run
1. Clone the repository  
   ```bash
   git clone https://github.com/your-username/booth-multiplier.git
