# CS50 C CLASS NOTES

Disclaimer: this might contain incorrect information! I am baby!

## Starter info, header files and boilerplate

C is a low-level language that requires more information from the coder than you'd expect from a higher-level language. This means that memory allocation is a factor to take into account when programming in C. It also matters which data types you use, as there are options that are more or less limited in size (for example, the data type `int` is used for 32-bit sized integers, but `long` is used for 64-bit integers).

CS50 requires using two extensions provided in the virtual codespace of the course. For the CS50 library: `#include <CS50.h>`. For the Standard input-output library: `#include <stdio.h>`.

Start with: `int main(void)` and open brackets `{}`.

## Functions and other monsters

* Printf: `printf("example");`. The first argument inside has to be a string. Type `/n` for new line.
* Get input: you assign a returned value to a variable, can be `variable = get_string("example ")`; other data type examples are int, char, etc. Inside the `printf` function, you can place format code inside the quotes in the form of a placeholder like `%s`, and follow the string with a comma and the variable name. For example:  
 `string answer = get_string("What's your name? ");`  
 `printf("Hello, %s\n", answer);`  
 Another way to write this:  
 `printf("Hello, %s\n", get_string("What's your name? "));`  
 This does not save the input in a variable that can be reused.

* Annotate by starting a line with `//`.
* Syntactic sugar: in designing a counter variable that repeatedly changes by the same amount, you can write it out as `counter = counter + 1;`, but also as `counter += 1;`. If you're only incrementing or decreasing by one, additionally, you can type it out as `counter++;`. You will need to specify the data type of the variable the first time you define it.

## Example programs

* Simple calculator (addition): this program adds integers. Get int input to declare `x` and `y` variables, and calculate in `printf("%i", x + y)`. To reuse the result variable instead, declare a `z` variable outside `printf`.

* Point comparison: this program compares the user's points to the coder's. Declare the variable by asking the user's amount of points. Then, use the constructs `if`, `else if`, and `if` to print answers telling the user whether they got more, less, or the same amount of points. For better design, declare a variable with the coder's number of points before the conditionals, so as to avoid hard-coding the number in several points of the code. To avoid accidentally changing a variable, add `const` to make the variable constant so it cannot be changed later in the code. It is a C convention to capitalize constant variables.

* 
