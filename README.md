# Express.js - Empty req.body Issue

This repository demonstrates a common issue in Express.js applications where `req.body` remains empty despite using the `express.json()` middleware to parse JSON payloads.

## Bug Description

The server successfully receives POST requests, but the `req.body` object is empty, preventing access to the request's JSON data.  This is a frequent problem, often caused by misconfiguration or incorrect middleware order.

## Solution

The solution involves ensuring that the `express.json()` middleware is placed before the route handler that expects JSON data. Also, the content-type header in the request must be set to application/json.  The corrected code is provided in `bugSolution.js`.