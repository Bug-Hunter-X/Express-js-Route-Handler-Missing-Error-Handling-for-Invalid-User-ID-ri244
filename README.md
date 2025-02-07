# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  the lack of proper error handling for invalid input.  Specifically, this example showcases a route that fetches a user by ID but fails to handle cases where the provided ID is not a valid integer.

## Bug
The `bug.js` file contains the buggy code.  It attempts to parse the user ID as an integer, but if the ID is not a valid integer (e.g., a string or a non-numeric value), the `parseInt` function will return `NaN`, causing errors and potentially crashing the application.

## Solution
The `bugSolution.js` file provides a corrected version of the code. The solution includes explicit checks to ensure the user ID is a valid integer before proceeding.  This prevents errors and provides a more robust and reliable route handler.

## How to Reproduce
1. Clone this repository.
2. Navigate to the directory containing `bug.js`.
3. Run the application (e.g., using `node bug.js`).
4. Send a request to `/users/<invalid_id>` (e.g., `/users/abc` or `/users/123a`).
5. Observe the error or unexpected behavior.
6. Repeat steps 2-5 using `bugSolution.js` to see the corrected behavior.