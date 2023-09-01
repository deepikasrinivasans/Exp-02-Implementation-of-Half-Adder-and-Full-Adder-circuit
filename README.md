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
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:*
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6.*Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.

## PROGRAM:
```
Developed by: Deepika S
RegisterNumber:  212222230028
```
### HalfAdder
```
module Experiment03(A,B,S,C);
input A,B;
output S,C;
assign S=A^B;
assign C=A&B;
endmodule
```
### FullAdder
```
module EX03(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=a^b^c;
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```
## RTL Diagram:
### HalfAdder
![ex03 rtl viewer](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/406c2883-9d91-412b-844d-39cfadf2f22d)
### FullAdder
![full adder rtl viewer](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/e616bce8-c93a-4084-9381-3fa835e55d3a)

## TRUTH TABLE:
### HalfAdder
![halfadder truthtable](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/64ec4ba5-ff81-4524-9f6e-270d74cdc2da)
### FullAdder
![fulladder truthtable](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/300df332-d8a8-4b11-b2fe-95875ac1a492)
## OUTPUT WAVEFORM:
### HalfAdder
![waveform halfadder](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/abf5dded-4285-4488-ba22-16679088518f)
### FullAdder
![WhatsApp Image 2023-09-01 at 9 52 01 AM](https://github.com/deepikasrinivasans/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119393935/a1c0e734-cd6f-4b3c-b563-a4d591696acd)
### Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
