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

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: FARHAAN THAYYIB L
RegisterNumber: 212225230069
*/
Full adder
```
module exp4(sum, carry, a, b, cin);
    output sum;
    output carry;
    input a;
    input b;
    input cin;

    assign sum = a ^ b ^ cin;
    assign carry = (a & b) | (cin & (a ^ b));
endmodule
```
Full subtractor
```
module exp42(diff, borrow, a, b, bin);
    output diff;
    output borrow;
    input a;
    input b;
    input bin;

    assign diff = a ^ b ^ bin;
    assign borrow = (a & b) | ((a ^ b) & bin);
endmodule
```
**RTL Schematic**
FULL ADDER
<img width="914" height="371" alt="image" src="https://github.com/user-attachments/assets/f94df3b9-f1c7-4657-ac91-bbcb28ca54ce" />

FULL SUBTRACTOR
<img width="941" height="356" alt="image" src="https://github.com/user-attachments/assets/c8fdef6d-e49c-4774-8013-8537ce8d4bc4" />

**Output Timing Waveform**
FULL ADDER
<img width="934" height="223" alt="image" src="https://github.com/user-attachments/assets/ed98cbd0-84d8-4af4-a588-df5ef39c5a1b" />

FULL SUBTRACTOR
<img width="941" height="318" alt="image" src="https://github.com/user-attachments/assets/1b618213-c435-4485-9fab-3d8aab5fee49" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



