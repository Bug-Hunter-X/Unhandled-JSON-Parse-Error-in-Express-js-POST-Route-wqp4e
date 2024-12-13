# Unhandled JSON Parse Error in Express.js POST Route

This repository demonstrates a common error in Express.js applications:  failure to handle malformed JSON data sent in the request body of a POST request.  The provided `bug.js` file shows the problematic code, while `bugSolution.js` offers a robust solution.

## Problem

The `bug.js` example uses `express.json()` middleware to parse JSON request bodies. However, it lacks error handling. If a client sends improperly formatted JSON, the application might crash or silently fail to process the request.  This can lead to difficult-to-debug production issues.

## Solution

The `bugSolution.js` file demonstrates how to properly handle potential JSON parsing errors using a try...catch block.  This ensures the server gracefully handles bad requests and prevents unexpected crashes.  A more informative error response is also sent back to the client.