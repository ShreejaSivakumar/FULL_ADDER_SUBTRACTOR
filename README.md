# FULL_ADDER_SUBTRACTOR
DATE : 25/11/2025
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
-------------------------------------
Full Adder
-------------------------------------
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


-------------------------------------
Full Sub
-------------------------------------
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




Developed by:  SHREEJA R S
RegisterNumber: 25017561
*/

**RTL Schematic**

-------------------------------------
Full Adder
-------------------------------------

<img width="926" height="577" alt="Screenshot 2025-11-25 214754" src="https://github.com/user-attachments/assets/b727d217-c4c2-4ba2-b9ba-2c3975fe081e" />

-------------------------------------
Full Sub
-------------------------------------

<img width="825" height="330" alt="Screenshot 2025-11-25 214900" src="https://github.com/user-attachments/assets/034a7f3a-faf7-495f-b9ea-5384902f6bec" />


**Output Timing Waveform**

-------------------------------------
Full Adder
-------------------------------------

<img width="875" height="439" alt="Screenshot 2025-11-25 215038" src="https://github.com/user-attachments/assets/2b0297ba-875f-4545-a5f3-27cfd3ddf65c" />

-------------------------------------
Full Sub
-------------------------------------

<img width="869" height="615" alt="Screenshot 2025-11-25 215232" src="https://github.com/user-attachments/assets/beedb14f-acbb-4112-8609-4cab08761e28" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

