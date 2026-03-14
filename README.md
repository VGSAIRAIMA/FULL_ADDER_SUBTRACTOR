# FULL_ADDER

Implementation-of-Full-Adder-circuit

**AIM:**

To design a Full Adder circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime


**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Truthtable**
![image]([https://de-iitr.vlabs.ac.in/exp/half-full-adder/images/2.2.png](https://theorycircuit.com/digital-electronics/full-adder-circuit-diagram-with-logic-ic/))
**Procedure**
```
Open Quartus Prime software.

Create a new project with project name and location.

Select the required device for the project.

Create a new Verilog HDL file.

Write the Full Adder Verilog program.

Save the file using .v extension.

Set the file as Top-Level Entity.

Compile the design using Start Compilation.

Open Simulation Waveform Editor and apply inputs A, B, and Cin.

Run the simulation and verify Sum and Carry outputs using the truth table.
```

**Program:**
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber: 212225040359
*/
module expfl(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule
```
**RTL Schematic**
![image](https://github.com/VGSAIRAIMA/FULL_ADDER_SUBTRACTOR/blob/main/expfl01.png)

**Output Timing Waveform**
![image](https://github.com/VGSAIRAIMA/FULL_ADDER_SUBTRACTOR/blob/main/expfl02.png)
**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



