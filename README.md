# Request Tracker Package

## Overview

The **Request Tracker Package** provides a simple and efficient solution to track and log requests in Node.js applications, particularly Express-based ones. By assigning a unique identifier to each request, this package simplifies debugging, monitoring, and tracing the flow of requests across services.

---

## Installation

Install the package using npm:

```bash
npm install @rishavtarway/request-tracker


## Features

- **Unique Request ID**  
  Automatically generates a unique ID (UUID) for each incoming request, ensuring traceability.

- **Middleware Support**  
  Provides easy-to-integrate middleware for Express applications, making it simple to use.

- **Async Local Storage**  
  Uses `async-local-storage` to store request-specific data, ensuring accessibility throughout the application's lifecycle.

- **Response Header**  
  Automatically appends an `X-Request-Id` header to all responses for external request tracking.

- **Logger**  
  Includes a built-in logger that automatically tags log messages with the request ID for contextualized logging.

- **Metadata Storage**  
  Allows the storage and retrieval of additional metadata (e.g., user ID, endpoint) associated with each request.
