# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency.  The `useEffect` hook is designed to perform side effects after every render, but if it's not properly managed with a dependency array, it can lead to unexpected behavior and performance issues.

## Problem
The `bug.js` file contains a `MyComponent` that updates the count state with the button click and uses the `useEffect` to log the updated count to the console.  The dependency array in the `useEffect` hook is missing the `setCount` function. This causes the component to re-render continuously, leading to an infinite loop of console logs and potentially freezing the browser.