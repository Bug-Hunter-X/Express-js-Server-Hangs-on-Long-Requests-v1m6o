# Express.js Server Hang on Long Requests

This repository demonstrates a common issue in Express.js applications where long-running requests can cause the server to hang, making it unresponsive.  The issue is that Express.js, by default, does not handle long-running operations efficiently, potentially blocking the event loop.  This leads to a frozen server until the long operation completes. This example simulates a long-running task using `setTimeout`. 

**Solution:**  Employ techniques like using asynchronous operations or a separate worker process to handle long-running requests, preventing them from blocking the main event loop.

## How to reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install`
4. Run `node server.js`
5. Observe that there is a delay of 5 seconds to receive the response.
6. Run `node server-fixed.js` for a better implementation using async/await to avoid blocking the main event loop.