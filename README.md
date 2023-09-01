## NAME: DEEPIKA S
## REGISTER NUMBER: 212222230028
# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasherSoftware – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

## PROCEDURE:

Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.
## PROGRAM:

Developed by: Deepika S
RegisterNumber:  212222230028
# HalfAdder
```
module Experiment03(A,B,S,C);
input A,B;
output S,C;
assign S=A^B;
assign C=A&B;
endmodule
```
# FullAdder
```
module EX03(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=a^b^c;
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```
## RTL Diagram:
# HalfAdder
![ex03 rtl viewer](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/406c2883-9d91-412b-844d-39cfadf2f22d)
# FullAdder
![full adder rtl viewer](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/e616bce8-c93a-4084-9381-3fa835e55d3a)

## TRUTH TABLE:
# HalfAdder
![halfadder truthtable](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/64ec4ba5-ff81-4524-9f6e-270d74cdc2da)
# FullAdder
![fulladder truthtable](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/300df332-d8a8-4b11-b2fe-95875ac1a492)
## OUTPUT WAVEFORM:
# HAlfAdder
![waveform halfadder](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/abf5dded-4285-4488-ba22-16679088518f)
# FullAdder



### Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
