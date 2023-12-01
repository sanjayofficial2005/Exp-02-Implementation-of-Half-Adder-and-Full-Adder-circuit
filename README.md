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
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: SANJAY.M
RegisterNumber:  23013084
*/
### half_adder:
```python
module half_adder(a,b,s,c);
output s,c;
input a,b;
assign s=a^b;
assign c=a&b;
endmodule
```

### full_adder:
```python
module full_adder(A,B,cin,S,cout);
input A,B,cin;
output S,cout;
assign S=A^B^cin;
assign cout=(A&B)| (B&cin)| (A&cin);
endmodule
```
Logic symbol & Truthtable
RTL realization

### Output:
half_adder:
![image](https://github.com/sanjayofficial2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148048602/bd1b1905-19fb-4a51-9ca6-e06fa655c4d5)
full_adder:
![image](https://github.com/sanjayofficial2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148048602/58f6d2e9-e0aa-465c-a8b5-e27eb467d8d4)



### RTL:
half_adder:
![Screenshot from 2023-12-01 09-29-20](https://github.com/sanjayofficial2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148048602/0f4ddac7-9e83-4554-be7f-abdb87dcf6a5)
full_adder:
![Screenshot from 2023-12-01 09-29-36](https://github.com/sanjayofficial2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148048602/18bc50cc-40be-46cd-ad15-099a1e331ed0)


### TIMING DIAGRAM


### TRUTH TABLE :
half_adder:
![Screenshot from 2023-12-01 09-28-53](https://github.com/sanjayofficial2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148048602/df53efb4-96f9-4fe6-ac50-880aa2220c8b)
full_adder:
![Screenshot from 2023-12-01 09-29-03](https://github.com/sanjayofficial2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148048602/78b375b2-0a33-4942-9fbb-98bad7ad8af7)


### Result:
The program Haly adder and full adder executed succesfully.
