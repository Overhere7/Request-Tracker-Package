# Request Tracker Package

## Overview

The **Request Tracker Package** provides a simple and efficient solution to track and log requests in Node.js applications, particularly Express-based ones. By assigning a unique identifier to each request, this package simplifies debugging, monitoring, and tracing the flow of requests across services.

---

## Installation

Install the package using npm:

```bash
npm install @rishavtarway/request-tracker

Features
Feature	Description	Priority
Unique Request ID	Generate a unique ID (UUID) for each incoming request.	High
Middleware Support	Provide Express-compatible middleware for easy integration.	High
Async Local Storage	Store request-specific data using async-local-storage.	High
Response Header	Add X-Request-Id to responses for external tracking.	High
Logger	Log messages with the request ID automatically included.	Medium
Metadata Storage	Allow storing additional metadata (e.g., user ID, endpoint).	Medium


Getting Started
1. Import the Package
javascript
Copy code
const requestTracker = require('@rishavtarway/request-tracker');
2. Use Middleware in Your Express App
javascript
Copy code
const express = require('express');
const requestTracker = require('@rishavtarway/request-tracker');

const app = express();

// Add request tracker middleware
app.use(requestTracker.middleware());

app.get('/', (req, res) => {
  const requestId = requestTracker.getRequestId();
  console.log(`Handling request with ID: ${requestId}`);
  res.send(`Your request ID is: ${requestId}`);
});

app.listen(3000, () => {
  console.log('Server is running on port 3000');
});
3. Log Messages with Contextual Information
javascript
Copy code
const logger = requestTracker.logger();

// Log a message
logger.info('This is a log message with the request ID.');
