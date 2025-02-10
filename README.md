# Closure Issue in JavaScript Loops

This repository demonstrates a common closure-related issue in JavaScript loops using `setTimeout`.  The example shows how the final value of `i` is logged instead of the intended value at each iteration.

## Bug Description

The `myFunction` uses a `for` loop and `setTimeout`.  The intention is to log the value of `i` at each iteration after a one-second delay.  However, due to how closures work in JavaScript, by the time the `setTimeout` callbacks execute, the loop has already completed, and `i` will hold its final value (10).

## Solution

The solution involves creating a closure that captures the current value of `i` using an immediately invoked function expression (IIFE).