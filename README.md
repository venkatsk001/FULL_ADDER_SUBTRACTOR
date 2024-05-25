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


Full Adder

![exp 04(1)](https://github.com/23002776/FULL_ADDER_SUBTRACTOR/assets/145742657/6f1e868f-c353-4b56-bffe-14ec912f7984)


Full subtractor

![exp-04(2)](https://github.com/23002776/FULL_ADDER_SUBTRACTOR/assets/145742657/d99749ba-3f09-4200-9361-10c63b2c5f29)

**Procedure**
1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**Program:**
```
module FULL_addsub(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
assign sum = a^b^cin;
assign carry = (a&b) | (b&cin) | (a&cin);
wire a0;
not (a0,a);
//Write syntax for full subtractor Borrow and Difference in data flow modelling
assign DIFF = a^b^cin;
assign BO = (a0&b) | (b&cin) | (a0&cin);
endmodule
```
**RTL Schematic**


![exp-04(3)](https://github.com/23002776/FULL_ADDER_SUBTRACTOR/assets/145742657/dedfdbb2-6f36-4031-971f-0eb9b31e68f3)



**Output Timing Waveform**


![exp-04(4)](https://github.com/23002776/FULL_ADDER_SUBTRACTOR/assets/145742657/63c21b87-0632-4549-aaf5-6aef497e8de4)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



