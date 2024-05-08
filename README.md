# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. */

## Developed By: AKASH. M
## Register Number: 212223240003
```
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
module Boolean_min(a,b,c,d,w,x,y,z,f1,f2);
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

and(s,x,y);
and(t,w,y);
and(u,ydash,z);
or(f2,s,t,u);
endmodule
```
## Truth Table:
![316294107-a6b8101c-bd3c-4b64-bc4a-f4a8962ac13a](https://github.com/aaron-h-2k5/BOOLEAN_FUNCTION_MINIMIZATION/assets/144250957/9d58f73d-24b1-4c4d-89eb-f2fd33b20b9d)

![316294144-348e89c8-b4d6-4c9e-8783-541ac0829105](https://github.com/aaron-h-2k5/BOOLEAN_FUNCTION_MINIMIZATION/assets/144250957/89a5b37e-718b-44ec-806f-153c2772eca4)


## RTL realization
![WhatsApp Image 2024-03-24 at 19 42 13](https://github.com/aaron-h-2k5/BOOLEAN_FUNCTION_MINIMIZATION/assets/144250957/14088aea-a05e-4c94-9d99-70855268bb7b)

## Output:

![WhatsApp Image 2024-03-24 at 19 52 51](https://github.com/aaron-h-2k5/BOOLEAN_FUNCTION_MINIMIZATION/assets/144250957/8c4ea2a1-dcff-4acb-bd42-7dc71fd58c9c)


## Result:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

