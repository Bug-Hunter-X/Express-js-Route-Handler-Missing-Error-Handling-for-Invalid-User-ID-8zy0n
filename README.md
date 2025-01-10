# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, the example shows a route that retrieves a user by ID.  If the provided ID is not a valid integer, the code will throw an error.

## Bug

The `bug.js` file contains the buggy code.  The route handler parses the user ID as an integer, but doesn't check if the parsing was successful or if the resulting integer exists in the `users` array.  This can lead to unexpected behavior or crashes.

## Solution

The `bugSolution.js` file provides the corrected code.  It includes checks to handle cases where the ID is not a valid integer, or if the user is not found.