# Unresponsive Node.js Server

This repository demonstrates a common Node.js issue: an unresponsive server caused by a long-running synchronous operation that blocks the event loop.  The `bug.js` file contains the problematic code. The `bugSolution.js` file shows how to fix this using asynchronous operations.  This leads to improved server responsiveness and prevents other requests from being processed.

## How to Reproduce

1. Clone this repository.
2. Run `node bug.js`.
3. Try to access the server (e.g., using `curl http://localhost:3000` or a web browser). You'll likely find that the server is unresponsive during the 5-second delay.

## Solution

The solution involves refactoring the code to avoid blocking the event loop.  This is typically done using asynchronous programming techniques like promises, async/await, or callbacks. The improved version of the code is in `bugSolution.js`.