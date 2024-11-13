                 *Data Modeling*

module half_adder_data(a, b, sum, carry);
input a, b;
output sum, carry;
//data flow modeling 
wire a1, b1;
xor (sum, a, b);
and (carry, a, b);
endmodule

                *Behavioral Modeling*

module half_adder_behavioral(a, b, sum, carry);
input a, b;
output reg sum, carry;
//Behavioral modeling 
always @(*)
begin
    {carry, sum} = a + b;
end
endmodule

                *Gate-Level Modeling*

module half_adder_gate(a, b, sum, carry);
input a, b;
output sum, carry;
//gate level modeling 
xor U1(sum, a, b);
and U2(carry, a, b);

endmodule

                   *Testbench*
`timescale 1ns/1ps
module half_adder_tb;
reg a, b;
wire sum, carry;

half_adder_uut(a,b,sum,carry);
initial begin
#100;a=0;b=0;
#100;a=0;b=1;
#100;a=1;b=0;
#100;a=1;b=1;
end
initial begin
#500
$finish();
end
endmodule 