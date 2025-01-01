# Node.js Server Unresponsiveness Bug

This repository demonstrates a common issue in Node.js applications: server unresponsiveness caused by long-running operations within request handlers.  The `serverBug.js` file contains code that simulates a 5-second delay, which can lead to the server appearing unresponsive if not properly handled.  The `serverSolution.js` file provides a solution using asynchronous operations to avoid blocking the main thread.

## How to Reproduce the Bug

1. Clone this repository.
2. Run `node serverBug.js`.
3. Make a request to `http://localhost:3000`.  Notice that it takes 5 seconds to respond.  During this time the server cannot accept other requests.

## Solution

The solution involves using asynchronous operations (e.g., `async/await`) or callbacks to avoid blocking the event loop.  Refer to the `serverSolution.js` file for a corrected implementation.