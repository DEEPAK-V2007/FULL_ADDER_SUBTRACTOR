Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
## FULL ADDER

<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/32971809-0306-4b53-8f53-b05db54d807d" />

## FULL SUBTRACTOR

<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/9dc86c86-8a0c-428e-bcdc-48ce24adf187" />

**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
## Developed by: DEEPAK.V
## RegisterNumber: 212225230044
*/
## FULL ADDER
```
module EXP4FULLADDER(A,B,Cin,Sum,Carry);
input A,B,Cin;
output Sum,Carry;
assign Sum=A^B^Cin;
assign Carry=A&B|B&Cin|A&Cin;
endmodule
```
## FULL SUBTRACTOR
```
module EXP4FULLSUBTRACTOR(A,B,Cin,Difference,Borrow);
input A,B,Cin;
output Difference,Borrow;
assign Difference=A^B^Cin;
assign Borrow=~A&B|B&Cin|~A&Cin;
endmodule
```
**RTL Schematic**
## FULL ADDER

![WhatsApp Image 2026-03-09 at 11 57 10 AM](https://github.com/user-attachments/assets/ae902bbf-fb2e-4db7-8a97-a6ab2899e532)

## FULL SUBTRACTOR

![WhatsApp Image 2026-03-09 at 12 03 22 PM](https://github.com/user-attachments/assets/9da7d823-4402-4b67-beeb-0d0b0a0a6d68)

**Output Timing Waveform**
## FULL ADDER

<img width="1600" height="848" alt="image" src="https://github.com/user-attachments/assets/6435c227-53a0-499a-9645-46cbd38141ac" />

## FULL SUBTRACTOR

![WhatsApp Image 2026-03-09 at 12 04 44 PM](https://github.com/user-attachments/assets/301fa8a4-5409-4b49-b22e-5fcb391ddb29)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



