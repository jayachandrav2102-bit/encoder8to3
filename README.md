Aim:

To design and implement an 8-to-3 priority encoder using Verilog (or digital logic) and verify its truth table and output.

Software Required:

Quartus prime

ModelSim (for functional simulation

Theory:

An encoder is a combinational circuit that converts 2^n input lines into an n-bit binary code.

A 8-to-3 encoder has 8 inputs (D0–D7) and 3 outputs (Y2, Y1, Y0).

Only one input should be high at a time (priority encoders handle multiple active inputs).

The output corresponds to the binary code of the active input line.

Procedure:

1.Open your Verilog IDE (Xilinx ISE/Vivado).

2.Create a new project and add a Verilog module named encoder8to3.

3.Declare 8 inputs (D0–D7) and 3 outputs (Y2–Y0).

4.Implement the logic equations using assign statements.

5.Compile and synthesize the design.

6.Simulate the design using a testbench to apply all input combinations.

7.Verify that the output matches the truth table.

Program:

~~~
module  encoder_8to3(
    input  wire [7:0] in,   // 4 input lines
    output reg  [2:0] out   // 2 output lines
);
    always @(*) begin
        case (in)
            8'b00000001: out = 2'b000;
            8'b00000010: out = 2'b001;
            8'b00000100: out = 2'b010;
            8'b00001000: out = 2'b011;
				8'b00010000: out = 2'b100;
				8'b00100000: out = 2'b101;
				8'b01000000: out = 2'b110;
				8'b10000000: out = 2'b111;
            default: out = 2'bxxx;  // Invalid case
        endcase
    end
endmodule

Developed by: JAYACHANDRA V
Register number:25017587*/


~~~
RTL LOGIC FOR ENCODER8-3

TIMING DIAGRAM FOR ENCODER8-3

Result:


 Thus the encoder 8 to 3 using verilog and validating their functionality using their functional tables is implemented and verified.

