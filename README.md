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


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
~~~
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
module ex2(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and (s,ydashz);
and (t,x,y);
and (u,w,y);
or (f2,s,t,u);
endmodule
~~~
Developed by: RegisterNumber:212223220024


**RTL realization**

**Output:**
![ex2 logic gate](https://github.com/gayathrimurugan12/BOOLEAN_FUNCTION_MINIMIZATION/assets/149365374/125f9701-6926-4cae-beec-9f6959b2cb03)
![ex2](https://github.com/gayathrimurugan12/BOOLEAN_FUNCTION_MINIMIZATION/assets/149365374/1bf69ce4-aa8e-41ac-af34-a7634c0743e9)

**RTL**

**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

