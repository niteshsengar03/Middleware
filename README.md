
# Express Middleware 

This repository contains three examples of middleware usage in Express.

## Request Count Middleware
- File: `requestCountMiddleware.js`
- Description: Increments a global variable `requestCount` for each incoming request.
- Endpoints:
  - `GET /user`: Returns user data.
  - `POST /user`: Creates a dummy user.
  - `GET /requestCount`: Returns the current value of `requestCount`.

## Error Handling Middleware
- File: `errorHandlingMiddleware.js`
- Description: Increments a global variable `errorCount` for each exception thrown in the endpoints. Returns a 404 status code to end users when an exception occurs.
- Endpoints:
  - `GET /user`: Throws an exception to simulate a user not found error.
  - `POST /user`: Creates a dummy user.
  - `GET /errorCount`: Returns the current value of `errorCount`.

## Rate Limiting Middleware
- File: `rateLimitingMiddleware.js`
- Description: Rate-limits requests from users to 5 requests per second. Blocks users with a 404 status code if they exceed the limit.
- Endpoints:
  - `GET /user`: Returns user data.
  - `POST /user`: Creates a dummy user.
- Header: Users should include their user ID in the header as 'user-id'.

## How to Use
1. Clone the repository.
2. Run each middleware file separately using Node.js.
3. Test the endpoints using tools like Postman.

## Dependencies
- Express.js

