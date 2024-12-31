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

![WhatsApp Image 2024-12-21 at 09 58 47_52e9e6cf](https://github.com/user-attachments/assets/3efbe0fa-d231-48d9-b455-38c87ca4b3a9)
![WhatsApp Image 2024-12-21 at 09 59 06_8dc1c8d7](https://github.com/user-attachments/assets/520081ec-95d5-4a6b-8431-f0a734b3b80d)


**Procedure**

1.Type the program in Quartus software. 2.Compile and run the program. 3.Generate the RTL schematic and save the logic diagram. 4.Create nodes for inputs and outputs to generate the timing diagram. 5.For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:  Swetha.k  RegisterNumber:  24900616
```
FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```


**RTL Schematic**
FULL ADDER
![WhatsApp Image 2024-12-27 at 10 37 48_1fbea839](https://github.com/user-attachments/assets/f67eb484-8a31-425a-8280-198d1c470e49)
FULL SUBTRACTOR
![WhatsApp Image 2024-12-27 at 10 38 44_b606f12b](https://github.com/user-attachments/assets/a8333b37-387e-4d41-b53d-99a08018c50a)

**Output Timing Waveform**
![WhatsApp Image 2024-12-27 at 10 38 56_c16ed566](https://github.com/user-attachments/assets/1b6e9d84-05aa-406d-a5a9-a24043c94f10)
![WhatsApp Image 2024-12-27 at 10 39 09_03548f14](https://github.com/user-attachments/assets/76dd7c9e-369a-4a1f-8b88-021f383f8816)


**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



