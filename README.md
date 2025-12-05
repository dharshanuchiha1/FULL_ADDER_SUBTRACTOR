# FULL_ADDER_SUBTRACTOR

**DATE : 05/12/2025**

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

Full Adder
-------------------------------------
// Full Adder in Verilog
```
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
```

Full Sub
-------------------------------------
// Full Subtractor in Verilog
```
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: DHARSHAN G
RegisterNumber: 25016421
*/

**RTL Schematic**

Full Adder
-------------------------------------

<img width="943" height="588" alt="Screenshot 2025-12-04 161355" src="https://github.com/user-attachments/assets/929f8b57-2409-451a-92d6-0a523ffcff16" />


Full Sub
-------------------------------------
<img width="913" height="350" alt="Screenshot 2025-12-05 132932" src="https://github.com/user-attachments/assets/2025626b-01ff-4876-ace0-e43a524c8512" />


**Output Timing Waveform**

Full Adder
-------------------------------------

<img width="1254" height="202" alt="Screenshot 2025-12-04 161645" src="https://github.com/user-attachments/assets/c51c1516-3d9d-4d09-8ab6-bfe59a2f0a34" />

Full Sub
-------------------------------------

<img width="1140" height="196" alt="Screenshot 2025-12-05 132916" src="https://github.com/user-attachments/assets/def3f30e-8e95-4dcc-b47e-4d0338fd3498" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.


.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..

..
.
.

.
.
.
.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
..
.
..
.
..
.
..
.
..
.
..
.
..

