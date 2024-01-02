# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
###Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder


Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.
Sum = A’B+AB’ =A ⊕ B Carry = AB


![image](https://github.com/Presilla27/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155127632/327cdfb7-5c08-41f3-aee3-8b6cd64af4d1)
Figure -01 HALF ADDER

##Procedure


Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.

##Program


module project_3(sum,carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule

##RTL Realization


![image](https://github.com/Presilla27/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155127632/85ca17d0-a590-4eae-bc8f-97b2ce0e7446)

##TIMING DIAGRAM


![image](https://github.com/Presilla27/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155127632/28d78992-5495-4365-9b5c-3105ca101647)

##TRUTH TABLE


![image](https://github.com/Presilla27/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155127632/b0adab89-c17f-4955-a114-86a652ded90b)

### Full Adder


Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

![image](https://github.com/Presilla27/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155127632/66973109-0211-42d8-a004-102bc9a210c1)

#### Figure -02 FULL ADDER 

##Program


module project_3_2(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule

##RTL Realization


![image](https://github.com/Presilla27/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155127632/135c9dac-0d2a-4424-a0c0-2d0588c7cf24)

##TIMING DIAGRAM


![image](https://github.com/Presilla27/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155127632/a9c97f9c-8c6d-4092-815b-c7b766fa7788)

##TRUTH TABLE


![image](https://github.com/Presilla27/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/155127632/529c0af6-dccb-45b0-ab24-6541cc4e27db)


## Result:


Thus the given logic functions are implemented and their operations are verified using verilog programming


