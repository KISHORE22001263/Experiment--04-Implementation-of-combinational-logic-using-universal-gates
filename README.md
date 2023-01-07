# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure:
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
 - Developed by: KISHORE.B  

 - RegisterNumber: 22001263 

## USING NAND:
module combilogicnand(a,b,c,d,f);  

   input a,b,c,d;
   
   output f;
   
   wire p,q,r;
   
   assign p=(~c & b & a);
   
   assign q=(~d & c & ~a);
   
   assign r=(c & ~b & a);
   
   assign f=(~(~p & ~q & ~r));
   
   endmodule  
   
   
## USING NOR:
module combilogicnor(a,b,c,d,f);

   input a,b,c,d;
   
   output f;
   
   wire p,q,r;
   
   assign p=( c & ~b & a);
   
   assign q=( d & ~c & a);
   
   assign r=( c & ~b & a);
   
   assign f=(~(~( p | q | r)));
   
   endmodule


## Output:
## USING NAND GATE:
## RTL:
![Screenshot_20230107_072227](https://user-images.githubusercontent.com/121484538/211155298-93101bd2-6a42-4441-bcc0-6dc2f8fbba87.png)


## TRUTH TABLE:
![Screenshot_20230107_074615](https://user-images.githubusercontent.com/121484538/211155358-32d50ef7-13b3-46be-86a2-ab615606a9e8.png)

## Timing Diagram:
![Screenshot_20230107_081337](https://user-images.githubusercontent.com/121484538/211156384-0980d885-14b2-412a-969d-26fe2fe55b01.png)

## USING NOR GATE:
## RTL:
![Screenshot_20230107_072805](https://user-images.githubusercontent.com/121484538/211156464-6e297a0d-9586-46de-b50e-6eb1d12f9f6a.png)
## TRUTH TABLE:
![Screenshot_20230107_074615](https://user-images.githubusercontent.com/121484538/211155358-32d50ef7-13b3-46be-86a2-ab615606a9e8.png)
## Timing diagram:
![Screenshot_20230107_082118](https://user-images.githubusercontent.com/121484538/211156685-7ebbcda7-ca0f-4016-82d6-d4fd3994e8df.png)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
