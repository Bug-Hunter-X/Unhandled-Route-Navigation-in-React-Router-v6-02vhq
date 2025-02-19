# React Router v6 Unhandled Route Navigation

This example demonstrates a common issue in React Router v6 where navigating to a path that doesn't have a corresponding route defined leads to unexpected behavior.  The application might render nothing, or unexpectedly render a different component, even if you have a catch-all route.

The `bug.js` file shows the initial, problematic code. The `bugSolution.js` file provides the corrected implementation.

## Problem:

The `App` component uses `Routes` and `Route` to define navigation routes.  However, if the user attempts to navigate to a route not explicitly defined, the application doesn't handle it gracefully.

## Solution:

The solution involves adding a catch-all route (`Route path="*"`) to handle any paths that are not explicitly defined. This ensures that a default component is rendered, preventing unexpected behavior or crashes.