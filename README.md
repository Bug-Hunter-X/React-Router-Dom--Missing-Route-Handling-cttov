# React Router Dom: Missing Route Handling

This repository demonstrates a common error in React Router Dom v6:  failure to handle routes that don't exist.  The application lacks a catch-all route (`/*`) or a specific route to handle unexpected paths, leading to unexpected behavior when navigating to invalid URLs. 

The `missingRouteBug.js` file shows the problematic code.  `missingRouteSolution.js` provides a solution.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/users` (or any other non-defined route). The application will not render a 404 page or display any content for that invalid route.

## Solution
The solution involves adding a `Route` component with `path="*"` to handle any unmatched paths, typically displaying a 404 page. See `missingRouteSolution.js` for implementation.