# Unexpected Results from calc() with Percentages in CSS

This repository demonstrates a common issue encountered when using the `calc()` function in CSS with percentage values.  Specifically, the problem arises when calculating a width based on a percentage minus a fixed pixel value, and the parent container's width is not explicitly defined or is determined indirectly (e.g., through flexbox or grid).

The `bug.css` file shows the problematic code, while `bugSolution.css` offers a solution.

## Problem
The issue stems from the order of operations and how the browser calculates the percentage before the subtraction. If the parent element's width isn't explicitly defined, the percentage calculation might be off, leading to incorrect results.

## Solution
Ensure the parent element has an explicitly defined width. This allows the browser to accurately perform the `calc()` operation.