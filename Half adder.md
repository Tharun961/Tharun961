
module half_adder(a,b,s,c);
input a,b;
output s,c;
//gate level modeling
xor t1(s,a,b);
and t2(c,a,b);
endmodule
    **TEST BENCH**
`timescale 1ns / 1ps
module ha_tb();
    reg a,b;
    wire s,c;
    ha uut(a,b,s,c);
    initial begin
    #100;a=0;b=0;
    #100;a=0;b=1;
    #100;a=1;b=0;
    #100;a=1;b=1;
    end
    initial begin
    #500;
    $finish();
    end
endmodule    
