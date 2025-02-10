# React Router v6 Catch-all Route Issue

This repository demonstrates an unexpected behavior in React Router v6 when using a catch-all route ("/*") in conjunction with other routes. The catch-all route, intended to handle 404 scenarios, seems to override other routes defined after it, even if those routes are more specific.

## Problem Description

The issue occurs when you define a catch-all route (`/*`) after other routes.  The catch-all route will be matched regardless of other more specific routes defined later. This is counter-intuitive to how catch-all routes generally function.

## How to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the application: `npm start`
4. Navigate to `/about`. You will see the 404 page instead of the About page, demonstrating the issue.

## Solution

The solution involves re-ordering the routes;  the catch-all route should always be placed last in the Routes component.