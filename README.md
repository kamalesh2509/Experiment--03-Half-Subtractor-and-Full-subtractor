# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

STEP 1: Use module projname(input,output) to start the Verilog programmming.

STEP 2: Assign inputs and outputs using the word input and output respectively.

STEP 3: Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

STEP 4: Use each output to represnt onre for differnce and the other for borrow.

STEP 5: End the verilog program using keyword endmodule.


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: kamalesh E
RegisterNumber: 212222100019

HALF SUBRACTOR:

module subractor(A,b,diff,borrow);
input A,b;
output diff,borrow;
wire X;
xor(diff,A,b);
not(X,A);
and(borrow,X,b);
endmodule


FULL SUBRACTOR:

module fullsub(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
wire p;
assign Diff = ((A^B)^C);
not(p,A);
assign Borrow = ((p&B)|(p&C)|(B&C));
endmodule
```

## Output:

## Truthtable

![230771064-4f02454c-bf80-4cf2-929e-0dc21506bffc](https://github.com/kamalesh2509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120444689/fbbf2a29-810e-42c8-8a03-0299a511f72c)
## LOGIC SYMBOL:

![230771153-9f852790-306e-47d7-b964-acefaaf248cb](https://github.com/kamalesh2509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120444689/cbf52291-26d5-49f3-9485-fe367196bed0)


##  RTL realization
![230771156-75435f12-3b6a-4df7-a28b-d63cb741cfe7](https://github.com/kamalesh2509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120444689/6256b5d8-f5e2-4190-b4e8-71f2c41ac73c)


## Timing diagram 
![230771165-a117a588-d83b-4d4e-9f87-eaa5f3f5b87e](https://github.com/kamalesh2509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120444689/a6c45c8b-1691-4a15-8713-48dab619bbf3)
## FULL SUBRACTOR:
## TRUTHTABLE:
![230771220-66c05ba6-028b-4b64-a4e0-3e57c978b148](https://github.com/kamalesh2509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120444689/70e0c5f2-d9ca-4981-993c-c5dcaf82560a)
## LOGIC SYMBOL:
![230771242-ddac95bd-1a72-41d6-9f68-c9b9ce1beeaf](https://github.com/kamalesh2509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120444689/0eeb1ef0-34cd-4bff-9678-96afb8f2475c)
## RTL REALIZATION:
![230771268-afb60885-cd82-4ab9-bd83-00931e0f46cc](https://github.com/kamalesh2509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120444689/db562df8-19a5-47c2-915e-e85626b76bc1)
## TIMING DIAGRAM:
![230771313-69d435b1-7308-42cd-93bb-217667842646](https://github.com/kamalesh2509/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120444689/93aecad8-4dee-4563-a686-515dcab66dba)


## Result:

Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
