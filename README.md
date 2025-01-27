# Unhandled Promise Rejection in Express.js Asynchronous Route Handler

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous route handlers.  When an asynchronous operation within a route handler throws an error and isn't properly caught, the server can crash without providing any meaningful feedback to the client.

The `bug.js` file shows the problematic code, while `bugSolution.js` offers a corrected version with proper error handling.

## Problem

The issue lies in the lack of comprehensive error handling within the asynchronous `someAsyncOperation` function. If the simulated error occurs, the promise rejection isn't caught, leading to a server crash.

## Solution

The solution involves adding a `catch` block to handle potential errors within the `then` chain of the promise.  Alternatively, using `async/await` with a `try...catch` block provides a more readable and structured approach to error handling.
