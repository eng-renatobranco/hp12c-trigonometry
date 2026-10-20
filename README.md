# HP-12C GOLD TRIGONOMETRY FUNCTIONS

The HP-12C is cheaper and easier to find than HP-15C, HP-11C and HP-35S and we want to use some RPN along our daily calculations.
But why do this with the HP-12C, if you can use some other scientific calculator to make your trigonometric calculations?... but why not?
In this way, I implemented some functions using the limited steps of the HP-12C.

Here we have the HP-12C program that implements five trigonometric functions, using 95 programming steps,
using X register for input and outup of the functions.

The implementation was developed based on published algorithms and performed well in some tests.
Although, it is not granted the precisions and the use of this program is up to you, at your own risk. It is provided as it is.

How to use:
* input in X -> g GTO NN -> R/S -> output in X
* sine / consine input must be in radians
* inverse functions returns in radians

We got:

| Function | Entry Point (NN) | Input (x) - X register | Output (x) - X register | Interval |
| --- | --- | --- | --- | --- |
| Sine | 01 | x in: real (rad) | sin(x) | [ -1 , 1 ] |
| Cosine | 82 | x in: real (rad) | cos(x) | [ -1 , 1 ] |
| Arcsine | 49 | x in: ] -1 , 1 [ | asin(x), rad | ] -pi/2 , pi/2 [ |
| Arccosine | 28 | x in: ] -1 , 1 ] | acos(x), rad | ] pi , 0 ] |
| Arctangent | 38 | x in: ] -inf , +inf [ | atan(x), rad | ] -pi/2, pi/2 [

Notes:
1. for limit values on arcsine and arccosine, it will take long time to converge and/or it will not converge at all;
2. for high values on arctangent, it will take a long time to converge and/or it will not converge at all;
3. to calculate tan(x) you must calculate sin(x) and divide by cos(x);
4. the program will use / erase / make useless of the data in Y, Z, and T registers;
5. the program uses the registers R0, R1, R2 and R3 as temp variables;
6. the registers R7, R8, and R9 will not be available in order of the program's size

## Program Input
To input the program you must clear the program memory of the calculator.


---- WARNING -----

IT WILL CLEAR ALL THE PROGRAM MEMORY OF THE CALCULATOR. BE AWARE THAT 
THIS PROCEDURE WILL ERASE ANYTHING THAT IS PREVIOUSLY PROGRAMED!!!!

---- WARNING -----


Press `f -> P/R` to enter in program mode.
Press `f -> PRGM` to clear the Program PGRM memory
Insert the steps presented in steps_hp12c-trig.txt
