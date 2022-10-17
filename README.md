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
### Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Yashaswi Mitta
RegisterNumber: 212221230062
*/
```
### Half Adder
```
module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
```
### Full Adder
```
module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```

### Output:
### Half Adder
### RTL

<img width="797" alt="output1" src="https://user-images.githubusercontent.com/93427522/190351879-2aead0b7-6ef8-4c3d-b57c-2c5dda048455.png">

### TIMING DIAGRAM

<img width="817" alt="output2" src="https://user-images.githubusercontent.com/93427522/190351908-d01a894e-e78a-43ea-a998-3a82c7999636.png">

### TRUTH TABLE 

<img width="772" alt="output3" src="https://user-images.githubusercontent.com/93427522/190351966-59b26797-fd69-4463-b050-c85dc5d23457.png">

### Full Adder
### RTL

<img width="708" alt="output4" src="https://user-images.githubusercontent.com/93427522/190352158-3dd29321-b35c-41f8-bd37-e6bb95fcc058.png">

### TIMING DIAGRAM

<img width="775" alt="output5" src="https://user-images.githubusercontent.com/93427522/190352241-833cde36-7257-4c7a-96eb-19bf0f854cff.png">

### TRUTH TABLE

<img width="787" alt="output6" src="https://user-images.githubusercontent.com/93427522/190352290-e1202d28-760d-4f2e-9287-dad87ef0a895.png">

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
