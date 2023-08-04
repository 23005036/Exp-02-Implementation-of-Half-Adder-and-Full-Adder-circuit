# Experiment-03 Implementation of Half Adder and Full Adder circuit

# Implementation ofHalf Adder and Full Adder circuit
#### NAME: BEATRICE THOMAS
#### Register no.: 23005036
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’C + A’BC’ + ABC + AB’C’ = A ⊕ B ⊕ C Carry = AB + AC + BC

### Procedure
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6. Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.


### Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

HALF ADDER:


<img width="402" alt="halfadder program" src="https://github.com/23005036/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035214/2fbd886e-edcc-440d-b812-24c1e7e58d0a">

FULL ADDER:


<img width="361" alt="fulladder program" src="https://github.com/23005036/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035214/a51be7a5-2942-48f1-8819-3a8e5ca8ee78">

#### HALF ADDER

module Halfadder(sum,a,b,carry);

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule 

RTL realization:


half adder:


<img width="364" alt="halfadder rtl" src="https://github.com/23005036/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035214/18f28ed6-d0f2-473a-957b-2fe4646062e5">

truth table:


![halfadder](https://github.com/23005036/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035214/4f60c7fa-3357-4c4a-965d-8511be5e4599)


timing diagram:

half adder:


![image](https://github.com/23005036/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035214/3612712b-06f3-4c2c-a857-de996ca66697)



FULL ADDER

 module fulladder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

xor(sum,a,b,c);

assign carry=a&b | b&c | a&c;

endmodule 

RTL Realization:
full adder


 <img width="335" alt="fulladder rtl" src="https://github.com/23005036/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035214/e99ebfb1-2de7-4250-b1ee-d1825ec45b86">

Truth table: full adder


![fulladder](https://github.com/23005036/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035214/1878f6a5-56ea-449c-a9ec-fa5414b58381)

Timing diagram: full adder


<img width="545" alt="fulladder waveform" src="https://github.com/23005036/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140035214/8ba2e701-3ffa-4663-ac8b-5738d39a41fd">

RESULT:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.




