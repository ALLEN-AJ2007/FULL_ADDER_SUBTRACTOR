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

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For differtent input combinations generate the timing diagram.
#Full Adder Truth Tabel


<img width="881" height="627" alt="Screenshot 2025-12-17 210729" src="https://github.com/user-attachments/assets/f8e173f8-6b54-482b-bc3d-dd07d0b94b0c" />


**Program:**
#FULL ADDER
```
module full_adder(
    input A, B, Cin,
    output Sum, Cout
);

assign Sum  = A ^ B ^ Cin;
assign Cout = (A & B) | (B & Cin) | (A & Cin);

endmodule
```
#Full Subtracter Truth Tabel


<img width="900" height="618" alt="Screenshot 2025-12-17 210952" src="https://github.com/user-attachments/assets/5ac8df42-2d7a-4c9c-a763-e2bec28de54f" />


#FULL SUBTRACTOR
```
module full_subtractor(
    input A, B, Bin,
    output Diff, Bout
);

assign Diff = A ^ B ^ Bin;
assign Bout = (~A & B) | (B & Bin) | (~A & Bin);

endmodule
```

**RTL Schematic**
#FULL ADDER

<img width="806" height="443" alt="Screenshot 2025-12-15 221959" src="https://github.com/user-attachments/assets/b89309f7-7732-410b-92d9-eeaac8f2053b" />

#FULL SUBTRACTOR

<img width="783" height="419" alt="Screenshot 2025-12-15 222127" src="https://github.com/user-attachments/assets/2d813ac7-6105-498f-b65d-6346a36f6341" />



**Output Timing Waveform**

<img width="806" height="172" alt="Screenshot 2025-12-15 222209" src="https://github.com/user-attachments/assets/24f20e90-df45-42eb-b165-e3e7a341e324" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



