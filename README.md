# Silent Failure in HTML DOM Manipulation

This repository demonstrates an uncommon bug in HTML related to accessing non-existent properties of elements added dynamically using `innerHTML`.  The issue is not that an error is thrown; rather, the attempt fails silently, which can be difficult to debug.

## Problem Description

The `bug.html` file illustrates the problem. We attempt to access a non-existent property of an element created via `innerHTML`. This access does not produce a helpful error message; instead, it appears to succeed without returning the expected `undefined`. This silent failure can lead to subtle and hard-to-find errors in web applications.

## Solution

The `bugSolution.html` file offers a safer approach. Instead of directly accessing the property, it uses the more robust `dataset` property to handle dynamically created elements, this prevents the unexpected behavior.

This repository serves as a learning tool for understanding this nuanced issue and avoiding similar problems in your own HTML and JavaScript code.