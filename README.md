# CSS `calc()` Pitfalls: Negative Values and Unit Inconsistency

This repository demonstrates a subtle but potentially problematic behavior of the CSS `calc()` function.  Specifically, it highlights the issues that arise when `calc()` produces negative values or when multiple, incompatible units are used together.

## Bug Description
The CSS `calc()` function allows for calculations within CSS properties. However, if the calculation results in a negative value (e.g., width becomes negative), the browser might handle this inconsistently, often defaulting to 0. Similarly, combining percentage units with other units (e.g., pixels, ems) can lead to unexpected and difficult-to-debug results.

## How to Reproduce
1. Clone this repository.
2. Open `bug.css` to see the problematic code.
3. Create an HTML file that references `bug.css`. Observe the rendered element's width in different scenarios (container width changes).
4. Compare the actual behavior with the expected behavior.

## Solution
The `bugSolution.css` file provides a possible way to handle this bug, or at least to be more aware of potential negative values when using `calc()`.  Thorough testing and careful unit handling are essential when using `calc()`.