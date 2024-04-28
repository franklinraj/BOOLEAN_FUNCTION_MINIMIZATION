# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


# Program:
```
Developed by: FRANKLIN RAJ G
RegisterNumber: 212223230058

module Boolean_min(A,B,C,D,W,X,Y,Z,F1,F2);
input A,B,C,D,W,X,Y,Z;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
output F1,F2;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign x6=(X)&(~Y)&(Z);
assign x7=(~X)&(~Y)&(Z);
assign x8=(~W)&(X)&(Y);
assign x9=(W)&(~X)&(Y);
assign x10=(W)&(X)&(Y);
assign F1=x1|x2|x3|x4|x5;
assign F2=x6|x7|x8|x9|x10;
endmodule
```
**RTL realization**

# Output:
![Screenshot 2024-04-28 194053](https://github.com/franklinraj/BOOLEAN_FUNCTION_MINIMIZATION/assets/148993740/d1b8c7b7-a2bc-4dfd-872e-66846c85df5f)


**Timing Diagram**
![Screenshot 2024-04-28 194118](https://github.com/franklinraj/BOOLEAN_FUNCTION_MINIMIZATION/assets/148993740/c2d74115-b821-4376-a62f-8f18752553c7)
![Screenshot 2024-04-28 194133](https://github.com/franklinraj/BOOLEAN_FUNCTION_MINIMIZATION/assets/148993740/306d02d5-0370-46d7-ac1b-f6a8b4c4da25)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

