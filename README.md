# Unhandled Exception in Asynchronous Callback in Node.js

This repository demonstrates a common error in Node.js applications: unhandled exceptions within asynchronous callbacks.  Improperly handling these exceptions can lead to application crashes and unexpected behavior.

## The Bug

The `bug.js` file contains a simple Express.js server.  It simulates an asynchronous operation (using `setTimeout`) that might fail.  If the simulated operation fails, an exception is thrown, but it's not caught, resulting in a server crash.

## The Solution

The `bugSolution.js` file shows how to properly handle this exception using `try...catch` blocks within the asynchronous callback, ensuring the server remains responsive even during errors.  The solution also includes error logging and sending an appropriate error response to the client.