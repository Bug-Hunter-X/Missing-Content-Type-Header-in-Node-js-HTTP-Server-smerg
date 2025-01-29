# Missing Content-Type Header in Node.js HTTP Server

This repository demonstrates a common error in Node.js HTTP servers: forgetting to set the `Content-Type` header.  This can lead to unexpected behavior in the browser, such as incorrect character encoding or the browser failing to render the response correctly.

The `bug.js` file shows the problematic code.  The `bugSolution.js` file provides the corrected code.

## How to Reproduce

1. Clone this repository.
2. Run `node bug.js`.
3. Open your browser and go to `http://localhost:3000`.
4. Observe the browser's behavior (it might not display the text correctly).
5. Run `node bugSolution.js`.
6. Re-open `http://localhost:3000` in your browser and observe the correct behavior.

## Solution

Always set the `Content-Type` header in your HTTP responses to ensure the browser correctly interprets the content.  The `bugSolution.js` file demonstrates the correct way to do this.