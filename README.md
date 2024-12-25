# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue in Express.js applications where JSON request bodies are not parsed correctly when a custom middleware is placed before `express.json()`.  The problem arises because the custom middleware might not handle the request body in a way that's compatible with `express.json()`.  This leads to `req.body` remaining empty or undefined, causing unexpected behavior.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` to install the required dependencies.
3. Run `node bug.js` to start the server.
4. Send a POST request to `http://localhost:3000/data` with a JSON payload (e.g., using Postman or curl).
5. Observe that the server logs an empty object for `req.body`.