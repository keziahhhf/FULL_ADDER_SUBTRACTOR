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
![318405960-7116d2bf-8e90-4e96-bfd5-d62af11a317a](https://github.com/keziahhhf/FULL_ADDER_SUBTRACTOR/assets/155235704/684c9df6-965b-48c9-899c-120f82c55fa4)

![fs](https://github.com/keziahhhf/FULL_ADDER_SUBTRACTOR/assets/155235704/2cd17651-9b5e-4896-97ee-9c10d853e565)

**Procedure**

Write the detailed procedure here

**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/


## Full_adder
module fulladd_top(a,b,cin,sum,carry);
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

## Full_subtractor
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule


Developed by: KEZIAH.F
RegisterNumber: 212223040094

**RTL Schematic**
![screen sht fa](https://github.com/keziahhhf/FULL_ADDER_SUBTRACTOR/assets/155235704/e0775026-d344-4001-bf6e-3e3e4b01c1b8)


**Output Timing Waveform**
FULL ADDER
![full adder](https://github.com/keziahhhf/FULL_ADDER_SUBTRACTOR/assets/155235704/77834984-e8b0-485c-80dc-f054ce76cbdd)

FULL SUBTRACTOR
![full subractor](https://github.com/keziahhhf/FULL_ADDER_SUBTRACTOR/assets/155235704/6aec80db-7bc5-41d2-a906-14e45cd6ec2d)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



