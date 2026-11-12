# cognevance_Digital-logic-Circuit-Design
Design and simulate basic digital logic circuits using Verilog/VHDL and simulation tools.

1. Scope and tools
The project includes basic logic gates, a half adder, a full adder, a 4:1 multiplexer, and a 4-to-2 priority
encoder. Verilog source files are provided in the rtl folder; the testbench is in testbench/. Xilinx Vivado
behavioral simulation is the target workflow. No FPGA board is required for functional simulation.
2. Theory and design
Logic gates: AND produces 1 when both inputs are 1; OR produces 1 when either input is 1; NOT inverts its
input. NAND, NOR, XOR, and XNOR are the corresponding complemented or exclusive operations.
3. HDL implementation
Each circuit is implemented as a separate Verilog module for reuse. digital_logic_top.v instantiates the
modules together as an integration wrapper. The designs are combinational and use continuous assignments
or an always @* block; no clock is required.
4. Verification strategy
The self-checking testbench applies all eight combinations of A, B, and Cin to verify the adders and logic
gates; all four MUX select values using data pattern 1010; and encoder cases covering no input, each single
input, and overlapping requests. It compares outputs against expected Boolean results using case inequality
(===/!==) and counts errors. A successful run prints: PASS: all test cases completed with zero errors
