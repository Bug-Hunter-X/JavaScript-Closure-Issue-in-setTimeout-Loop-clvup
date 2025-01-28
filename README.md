# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue within a `setTimeout` loop.  The problem arises because the loop variable `i` is not captured correctly within the `setTimeout` callback function.

## Bug Description
The expected behavior is to log the numbers 0 through 9 with a one-second delay between each number.  However, due to the closure issue, the loop completes before the `setTimeout` callbacks are executed, resulting in all callbacks logging the final value of `i` (which is 10). 

## Bug Solution
The solution involves using a closure to create a new variable scope for each iteration of the loop, ensuring that the correct value of `i` is captured for each callback.