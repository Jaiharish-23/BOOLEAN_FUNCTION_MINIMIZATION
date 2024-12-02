# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**
Implementing Boolean functions in Verilog HDL (Hardware Description Language) involves translating the simplified Boolean expressions into Verilog code to describe the behavior of digital circuits. The basic building blocks in Verilog is module. The module represent a combinational circuit. Use logical operators (&, |, ~, ^) to implement Boolean functions directly. Use built-in gate primitives for basic functions. Use University program VWF to verify the functionality of your Verilog modules. Create waveform and check outputs against expected results

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: JAI HARISH R
RegisterNumber: 24006817
*/

```
module boolean_function_minimization(a, b, c, d, w, x, y, z, f1, f2);
input a, b, c, d, w, x, y, z;
output f1, f2;
wire x1, x2, x3, x4, x5, x6, x7, x8, x9, x10;
assign x1 = (~a) & (~b) & (~c) & (~d);
assign x2 = (a) & (~c) & (~d);
assign x3 = (~b) & (c) & (~d);
assign x4 = (~a) & (b) & (c) & (d);
assign x5 = (b) & (~c) & (d);
assign f1 = x1 | x2 | x3 | x4 | x5;
assign x6 = (x) & (~y) & (z);
assign x7 = (~x) & (~y) & (z);
assign x8 = (~w) & (x) & (y);
assign x9 = (w) & (~x) & (y);
assign x10 = (w) & (x) & (y);
assign f2 = x6 | x7 | x8 | x9 | x10;
endmodule
```

**Output:**
**RTL realization**
![Screenshot (178)](https://github.com/user-attachments/assets/e2208fb8-35b2-45f0-82f3-997ea5e8d1c4)

**truth table**
```
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
```
![table1](https://github.com/user-attachments/assets/e5cf3c14-2e33-42dc-b9bc-cfe22ad5d883)
```
F2=xy’z+x’y’z+w’xy+wx’y+wxy
```

![table2](https://github.com/user-attachments/assets/8a1a27f1-f3ec-4c81-991b-21e6d2c2daaf)


**Timing Diagram**
![Screenshot (179)](https://github.com/user-attachments/assets/5d9bb7d7-eed1-4b09-a1de-04670e864e38)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

