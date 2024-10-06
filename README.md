### DEVELOPED BY: DAPPILI VASAVI
### REGISTER NUMBER:212223040030
# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

## AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Full Adder and Full Subtractor:

## Full Adder:

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

## Figure -1 FULL ADDER:

## Full Subtractor:

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## Truthtable:
### FULL ADDER:
![image](https://github.com/user-attachments/assets/88a530da-5994-4c2b-8297-55baaca5d8fe)


### FULL SUBTRACTOR:
![image](https://github.com/user-attachments/assets/92e86eaf-ef4a-43c6-b0b3-43de9253220b)


## Procedure:

Write the detailed procedure here

## Program:
### FULL ADDER:
```
module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule
```
### FULL SUBTRACTOR:
```
module fullsub(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
## RTL Schematic:
## FULL ADDER:
![image](https://github.com/user-attachments/assets/14dcabea-f219-4aa6-a159-9c1994a2b8b1)

## FULL SUBTRACTOR:
![image](https://github.com/user-attachments/assets/61479c49-811e-4087-8848-c9082a002ddd)

## Output Timing Waveform:
### FULL ADDER:
![image](https://github.com/user-attachments/assets/340a43c1-4ef6-4d34-a3bd-79b2d20f40fd)

### FULL SUBTRACTOR:
![image](https://github.com/user-attachments/assets/b3a5f940-85b0-4ea1-9507-d55d733bf60d)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



