# Experiment--04-Implementation-of-combinational-logic-using-universal-gates-
 ## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate


## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
 
 
 
 


## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.


 


## Program:
~~~ /*
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.
Developed by: Ravuri sathwik
RegisterNumber:  2000
*/~~~ 

## F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

module Combination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule
## F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

module norcombination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
not(F,S);
endmodule

~~~



## Output:
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

## Truthtable
![1 1111](https://user-images.githubusercontent.com/103410316/167441866-23fd1566-fa1c-43ed-8f80-52e7962276d9.png)



##  RTL realization

![1 22222](https://user-images.githubusercontent.com/103410316/167441907-979a8496-7ae3-4e0b-ba05-42f0c9fcfd82.png)


## Timing diagram 

![1 3333333333333](https://user-images.githubusercontent.com/103410316/167441919-43b40449-11a1-43b2-9420-190d7ad7e675.png)



F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

## Truthtable
![1 3333](https://user-images.githubusercontent.com/103410316/167441934-f7181619-5b50-48fb-9955-b0febe450b8c.png)


##  RTL realization

![1 444444](https://user-images.githubusercontent.com/103410316/167441967-2b8c4e3c-6b22-4942-a5bd-2c3321aca8e1.png)

## Timing diagram 
![1 55555](https://user-images.githubusercontent.com/103410316/167441988-91a5d8ea-0130-46cc-9e8b-3ff5e09f8cab.png)


## Result:
Thus implementation of logic functions using NAND and NOR gates is done and its operation is verified in Quartus using Verilog programming.
 
