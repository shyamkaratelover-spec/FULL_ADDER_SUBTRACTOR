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

<img width="585" height="260" alt="image" src="https://github.com/user-attachments/assets/017bbbba-4645-4f4e-b241-5634f760d385" />

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

<img width="382" height="268" alt="image" src="https://github.com/user-attachments/assets/dae1e019-784d-4252-8273-32463b0705a7" />

**Procedure**

Write the detailed procedure here

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
 ~~~
Developed by: SHYAM M
RegisterNumber: 212225220096
~~~
~~~
FULL ADDER

module exp3(sum, cout, a, b, cin);
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

FULL SUBTRACTOR

module fullsub(df, bo, a, b, bin);

    output df;
    output bo;
    input a;
    input b;
    input bin;

    assign df = a ^ b ^ bin;
    assign bo = (~a & b) | (~(a ^ b) & bin);

endmodule
~~~


**RTL Schematic**

**Output:
FULL ADDER

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2d7fcd4f-7c0a-4fc0-9f76-13395df286b0" />
FULL SUBTRACTOR

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5065adf4-1b3f-4c60-b3f8-144928b03e83" />

Timing Waveform**
FULL ADDER

<img width="1920" height="1080" alt="Screenshot (156)" src="https://github.com/user-attachments/assets/abf38b6e-effc-4de0-ab7f-85773738be2a" />

FULL SUBTRACTOR

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cba379f0-86da-47fe-92c1-5374aa939fde" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



