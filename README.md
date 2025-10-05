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

<img width="774" height="544" alt="388824508-b09e7332-958e-4e84-9f53-7affd2357d9c" src="https://github.com/user-attachments/assets/99cd490e-4985-4c7a-9810-41499561edb5" />


**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

<img width="825" height="566" alt="388824554-ca8e58aa-8470-42ed-8d58-e2f5effe7f02" src="https://github.com/user-attachments/assets/f7e01179-76d4-49b5-b216-34b3534869b1" />


Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

FULL ADDER

<img width="429" height="395" alt="388825036-4d112be1-6902-42f6-a80f-d6ffa1814c34" src="https://github.com/user-attachments/assets/f3c1335f-3cf1-4e8f-9513-1f132bbc48ad" />

FULL SUBRACTOR

<img width="438" height="393" alt="388825191-affd2a74-295b-48dc-b7c5-3e2de75db7d3" src="https://github.com/user-attachments/assets/b362a206-74ce-49c4-be5e-b10910806467" />

**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

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
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));    
endmodule    

Developed by:DHARSHINI V

RegisterNumber:25010872

**RTL Schematic**

FULL ADDER

<img width="1920" height="1080" alt="Screenshot (28)" src="https://github.com/user-attachments/assets/5ca3ce65-b255-4031-a47d-3bf57a4f062b" />

FULL SUBTRACTOR

<img width="1920" height="1080" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/57ce345f-ae30-4c23-b8c5-822ff958e254" />

**Output Timing Waveform**

FULL ADDER

<img width="1920" height="1080" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/f916385c-cd4f-4495-8c65-665fa5208023" />

FULL SUBTRACTOR

<img width="1920" height="1080" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/a89c80ee-a841-4aa3-ac28-bac2c29f7f4a" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



