# Node.js Server Resource Exhaustion

This repository demonstrates a common Node.js error: resource exhaustion due to improperly handled connections in an HTTP server. The `server.js` file contains the buggy code, while `serverSolution.js` provides the corrected version.

## Problem

The original server code creates an HTTP server but fails to properly manage connections.  This leads to an ever-increasing number of open connections, ultimately exhausting system resources and causing the server to become unresponsive or crash.

## Solution

The solution involves explicitly closing the connection after handling the request using `res.end()` and employing appropriate error handling to gracefully manage potential issues.