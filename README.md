# cognevance_Digital-logic-Circuit-Design
Design and simulate basic digital logic circuits using Verilog/VHDL and simulation tools.

module level1(
 input a, b, cin,
   output sum, cout
);

assign sum = a ^ b ^ cin;

assign cout = (a & b) |
             (a & cin) |
             (b & cin);
endmodule
