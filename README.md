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

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
FULL ADDER:
<img width="482" height="404" alt="Screenshot 2025-10-07 132423" src="https://github.com/user-attachments/assets/56a16f8b-aba5-429d-8e22-9411864d7855" />

FULL SUBTRACTOR
<img width="488" height="336" alt="Screenshot 2025-10-07 133019" src="https://github.com/user-attachments/assets/5c450129-5649-419f-97b2-2efcfa2d4864" />






**Procedure**


1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule

**RTL Schematic**
FULL ADDER:
<img width="1721" height="817" alt="Screenshot 2025-10-07 130829" src="https://github.com/user-attachments/assets/8139c5f5-a19c-4924-b6eb-c7e8bd9727af" />

FULL SUBTRACTOR:
<img width="745" height="301" alt="Screenshot 2025-10-07 133441" src="https://github.com/user-attachments/assets/beabb0c1-616c-4167-815b-aaec22f77d15" />


**Output/TIMING Waveform**
FULL ADDER:
<img width="902" height="299" alt="Screenshot 2025-10-07 133537" src="https://github.com/user-attachments/assets/9e44acf9-1c56-42e2-8acf-8f72f33cd9a0" />

FULL SUBTRACTOR:
<img width="901" height="277" alt="Screenshot 2025-10-07 133610" src="https://github.com/user-attachments/assets/4023cdb2-1347-4db1-8311-37f76ff69817" />


**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is
 verified using Quartus software.

