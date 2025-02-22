# React useEffect Fetch: Handling Aborted Requests on Unmount

This example demonstrates a common issue when using the `useEffect` hook with `fetch` in React.  If the component unmounts before the fetch request completes, the promise might still resolve, leading to errors and warnings because the component is no longer mounted.  This repository shows the buggy code and the solution.

## Bug

The `bug.js` file contains the buggy implementation.  It uses `AbortController` to handle fetch cancellation, but it's missing crucial error handling and data management after the abort.

## Solution

The `bugSolution.js` file demonstrates the correct implementation.  It handles potential errors and data manipulation when a fetch request is aborted.