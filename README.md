# Node.js Server Hang

This repository demonstrates a common Node.js issue: a server hanging due to a long-running synchronous operation that blocks the event loop. The `server.js` file contains the buggy code, while `serverSolution.js` provides the corrected implementation.  The bug causes the server to become unresponsive to new requests while the synchronous operation is in progress.  The solution employs asynchronous techniques to prevent this blocking behavior.

## Bug

The synchronous `while` loop in the request handler simulates a long-running task. This blocks the event loop, causing the server to hang and preventing it from responding to other incoming requests.

## Solution

The solution uses asynchronous techniques to avoid blocking the event loop.  This allows other requests to be processed concurrently, preventing the server from hanging.