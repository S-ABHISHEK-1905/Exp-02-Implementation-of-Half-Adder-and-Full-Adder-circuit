# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
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

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: S.ABHISHEK

RegisterNumber: 212221230002 


HALF ADDER

module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

FULL ADDER

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```

### Output:
### Half adder:
### LOGIC SYMBOL:
![image](https://user-images.githubusercontent.com/94165326/165720028-af2df52c-25f0-4710-a31c-198a9763320d.png)

### RTL
![image](https://user-images.githubusercontent.com/94165326/165720076-486556c6-f578-4632-9345-567509a8e06d.png)

### TIMING DIAGRAM
![image](https://user-images.githubusercontent.com/94165326/165720124-ba882127-bdaf-47ca-a7b6-b435ed15fe7d.png)



### TRUTH TABLE 
![image](https://user-images.githubusercontent.com/94165326/165720162-dd4d71d7-5bda-44e9-a3d9-1df57c196550.png)

### FULL ADDER:
### LOGIC SYMBOL:
![image](https://user-images.githubusercontent.com/94165326/165720301-878e28d8-2deb-4f2c-a978-73abe98ee27e.png)
### RTL:
![image](https://user-images.githubusercontent.com/94165326/165720364-cfa8dd30-2b1a-4b4b-b899-4aac4cf86e6c.png)
### TIMING DIAGRAM:
![image](https://user-images.githubusercontent.com/94165326/165720480-ae2f67b5-2959-4c96-8855-966c93a5141d.png)
### TRUTH TABLE:
![image](https://user-images.githubusercontent.com/94165326/165720581-2f50e047-937d-4579-8373-365fa9d37fcd.png)



### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
