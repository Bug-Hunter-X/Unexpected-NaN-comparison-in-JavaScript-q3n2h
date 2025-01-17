# JavaScript NaN Comparison Bug

This repository demonstrates a common, yet subtle, bug in JavaScript related to the comparison of NaN (Not a Number) values.

## The Problem

In JavaScript, NaN is a special value that represents an invalid numerical result.  The peculiar behavior of NaN is that it's never equal to itself, neither using loose (`==`) nor strict (`===`) equality.

The `bug.js` file showcases this issue with a simple function that attempts to compare two numbers for equality.

## The Solution

The solution involves using `Number.isNaN()` to reliably check if a value is NaN.  This function correctly identifies NaN, avoiding the pitfalls of direct comparison.  The `bugSolution.js` file provides a corrected version of the function. 

## How to reproduce

1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` in your preferred JavaScript environment.
3. Run the code and observe the output.  You'll notice that the original function incorrectly reports `NaN` as unequal to `NaN`. The solution correctly identifies them as NaN.
