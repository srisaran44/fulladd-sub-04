AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

Full Adder and Full Subtractor

Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin

Carry = AB + ACin + BCin

image

Figure -1 FULL ADDER

Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

image

Diff = A ⊕ B ⊕ Bin

Borrow out = A'Bin + A'B + BBin

Truthtable

Procedure

Write the detailed procedure here

Program:

module EXP4(a,b,sum, cin, carry, bin, BO, DIFF);
input a,b,cin, bin;
output sum, carry, BO, DIFF;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(a&cin));
assign diff=(a^b^bin);
assign BO=((~a&b)|(~a&bin)|(b&bin));
endmodule
Developed by: J.SRI SARAN  RegisterNumber:25015592

OUTPUT;
<img width="669" height="333" alt="Screenshot 2025-12-27 132507" src="https://github.com/user-attachments/assets/477a9763-8b21-4a1c-902c-1f0e2be50759" />
<img width="830" height="357" alt="Screenshot 2025-12-27 132541" src="https://github.com/user-attachments/assets/0dc19e76-4042-4620-be83-d589f2050585" />

<img width="1045" height="772" alt="Screenshot 2025-12-27 132628" src="https://github.com/user-attachments/assets/11442b9d-b307-4168-a1a2-3526d074eea7" />




<img width="1032" height="268" alt="Screenshot 2025-12-27 132722" src="https://github.com/user-attachments/assets/e7f099d6-1274-421c-911c-2bd0cf7b6e51" />




Result:
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.

