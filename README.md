# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications: server unresponsiveness due to long-running operations within the request handler.  The `bug.js` file shows a server that hangs for 5 seconds during each request, making it unresponsive to other requests.  The solution is provided in `bugSolution.js`.

## Problem

Node.js is single-threaded.  If a long-running operation blocks the event loop, the entire server becomes unresponsive to new requests.  The example code uses a `while` loop to simulate such an operation.

## Solution

The solution involves using asynchronous operations or offloading long-running tasks to worker threads or other processes to prevent blocking the main thread and event loop.