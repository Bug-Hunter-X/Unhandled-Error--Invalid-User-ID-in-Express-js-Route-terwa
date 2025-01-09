# Unhandled Error: Invalid User ID in Express.js Route

This repository demonstrates a common error in Express.js route handlers:  failure to handle cases where input data is invalid or missing.  Specifically, this example shows a route that fetches a user by ID, but doesn't handle non-numeric IDs.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides a corrected version with proper error handling.

## Bug:
The original code attempts to parse the user ID as an integer using `parseInt()`, but doesn't check if the result is a valid integer or handle the case where `parseInt()` returns `NaN`. This can lead to unexpected behavior or crashes, particularly if the `users` array is accessed with a non-numeric index.

## Solution:
The corrected code includes checks to ensure the user ID is a valid integer before attempting to access the `users` array.  It also uses a more robust approach to handle the case where the user is not found, ensuring the server responds with a proper HTTP status code.