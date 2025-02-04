# JavaScript Loose Typing Bug

This repository demonstrates a common JavaScript bug caused by the language's loose typing system.  The `foo` function intends to add two numbers, but due to the implicit type coercion, it performs string concatenation when one of the arguments is a string.

## Bug Description
The core issue lies in the lack of strict type checking in JavaScript.  When a number and a string are used in the `+` operator, JavaScript automatically converts the number to a string before performing concatenation instead of throwing an error or performing numerical addition.  This behavior can lead to unexpected results and difficult-to-debug errors in larger programs.

## How to Reproduce
1. Clone this repository.
2. Run `node bug.js`.
3. Observe the output, which unexpectedly concatenates the number and string.

## Solution
The solution involves explicit type checking and/or conversion to ensure that both arguments are numbers before performing the addition operation.  The `bugSolution.js` file provides a corrected version of the `foo` function that demonstrates this solution.