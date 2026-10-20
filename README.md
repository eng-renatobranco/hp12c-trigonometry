# HP-12C GOLD TRIGONOMETRY FUNCTIONS

The HP-12C is cheaper and easier to find than HP-15C, HP-11C and HP-35S and we want to use some RPN along our daily calculations.
But why do this with the HP-12C, if you can use some other scientific calculator to make your trigonometric calculations?... but why not?
In this way, I implemented some functions using the limited steps of the HP-12C.

Here we have the HP-12C program that implements five trigonometric functions, using 95 programming steps, using X register for input and outup of the functions.

The implementation was developed based on published algorithms and performed well in some tests. Although, it is not granted the precisions and the use of this program is up to you, at your own risk. It is provided as it is.

How to use:
* input in X -> g GTO NN -> R/S -> output in X
* sine / consine input must be in radians
* inverse functions returns in radians

We got:

| Function | Entry Point (NN) | Input (x) - X register | Output (x) - X register |
| --- | --- | --- | --- |
| Sine | 01 | x real (rad) | sin(x) [-1,1] |
| Cosine | 82 | x real (rad) | cos(x) [-1,1] |


