# FULL_ADDER_SUBTRACTOR

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

i)FULL ADDER

![Screenshot 2024-12-16 082822](https://github.com/user-attachments/assets/1102029e-01cd-4b53-93e0-9cc72046d0e3)

ii)FULL SUBTRACTOR


![Screenshot 2024-12-16 082827](https://github.com/user-attachments/assets/a472e3d6-34ae-4f36-8cd1-4c4a4d5eac24)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:vishwa v

RegisterNumber:24901061

*/

```
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
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```

**RTL**

i)FULL ADDER

![Screenshot 2024-12-16 082838](https://github.com/user-attachments/assets/0c89329e-143c-4d11-9508-74272b8079aa)

ii)FULL SUBTRACTOR


![Screenshot 2024-12-16 082850](https://github.com/user-attachments/assets/adcbc76a-dbb4-4f7f-b9f2-2b35dcbab68b)

**Output**

i)FULL ADDER


![Screenshot 2024-12-16 082911](https://github.com/user-attachments/assets/8c8d2ecb-9263-4c7c-b72a-627dfe7840a3)

ii)FULL SUBTRACTOR


![Screenshot 2024-12-16 082928](https://github.com/user-attachments/assets/7fb48ec2-bfb0-4f0e-90dd-f0b094b38954)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



