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

Program to design a half adder and full adder circuit and verify its truth table in quartus 
using Verilog programming. 

Developed by: Aakash P

Register Number: 22005471

### HALF ADDER: 
````
module add(a,b,sum,carry); 

input a,b; 

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule
````
### FULL ADDER:
````
module fulladd(a,b,c,sum,carry);

input a,b,c;

output sum,carry; 

assign sum = ((a^b)^c);

assign carry = ((a&b)|(b&c)|(c&a));

endmodule 
````

### Output:
### HALF ADDER:
### RTL realization:

![Screenshot (22)](https://user-images.githubusercontent.com/118799103/211162156-4c6c0104-f423-48ad-922b-5c65b54186db.png)

### TIMING DIAGRAM

![Screenshot (23)](https://user-images.githubusercontent.com/118799103/211162193-1b787040-f14f-440e-a8b2-acf68fc797ff.png)

### TRUTH TABLE 

![Screenshot (25)](https://user-images.githubusercontent.com/118799103/211162260-e0bf17e3-fb29-4da0-826b-5cd5675d15a6.png)

### FULL ADDER:
### RTL realization:

![Screenshot (27)](https://user-images.githubusercontent.com/118799103/211162295-e1e52689-a8a3-400f-b42a-8d079dc59d28.png)
### TIMING DIAGRAM:

![Screenshot (28)](https://user-images.githubusercontent.com/118799103/211162309-a8eada59-6ae9-4eb3-96bb-d5929039dd4b.png)
### TRUTH TABLE:

![Screenshot (30)](https://user-images.githubusercontent.com/118799103/211162345-1b1a61df-3d41-4198-b1e4-1ed610a28342.png)
### Result:

Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using 
Verilog programming.
