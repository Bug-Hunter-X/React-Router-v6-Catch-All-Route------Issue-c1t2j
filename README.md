# React Router v6 Catch-All Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router v6.  The catch-all route unintentionally intercepts other routes, even when those other routes should be matched.

The issue is described in detail in the `bug.js` file. The solution is provided in the `bugSolution.js` file. The solution involves a more specific route order or using a different approach for handling not found pages.

## Setup

1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`. 

## Problem Description

The main problem occurs when routing to other paths than `/` the `NotFound` component is rendered, this behavior is not expected, as the `/*` route should only match routes that are not matched by the other paths.

## Solution Description

The solution is to make the `/*` route the last path to be evaluated. This way, the other paths will be matched before the `/*` path is evaluated.