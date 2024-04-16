# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/GOWTHAM54577/HALF_ADDER_SUBTRACTOR/assets/144589420/c5154d8d-53b7-4301-9cae-efd77330e3aa)


Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/GOWTHAM54577/HALF_ADDER_SUBTRACTOR/assets/144589420/1b2acbf4-b964-4409-9bef-399c114fd2d5)


Figure -02 HALF Subtractor

**Truthtable**
Figure - 01 : Half adder
![image](https://github.com/Renusri-Naraharasetty/HALF_ADDER_SUBTRACTOR/assets/146916363/dc24f4df-8167-474f-830c-4eb545f4da3b)

Figure - 02 : Half subtractor
![image](https://github.com/GOWTHAM54577/HALF_ADDER_SUBTRACTOR/assets/144589420/dcd2e2e5-7581-41d1-bb1d-0bd52bc9cc2c)



**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: RENUSRI NARAHARASHETTY

RegisterNumber: 212223240139
*/
HALF ADDER:
```
module half_adder(a,b,sum,carry);
input a,b;
output sum,carry; 
assign sum = a^b;
assign carry = a & b;
endmodule
```

HALF SUBTRACTOR:
```
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
  assign Bo = ~a & b;
endmodule
```

**RTL Schematic**

**Output/TIMING Waveform**
# HALF ADDER:
![image](https://github.com/GOWTHAM54577/HALF_ADDER_SUBTRACTOR/assets/144589420/953a357f-965a-45e5-9dec-f2fb89670d2b)


# HALF SUBTRACTOR:
![image](https://github.com/GOWTHAM54577/HALF_ADDER_SUBTRACTOR/assets/144589420/c32279bd-2062-470d-9b4d-94564f261933)



**Result:**
Therefore the code has been run successfully and the output has been verified.
