# React useEffect Cleanup Function Missing

This repository demonstrates a common React bug involving a missing cleanup function in the `useEffect` hook.  The bug causes a memory leak by failing to clear an interval, leading to potential performance degradation.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## Bug
The `useEffect` hook in `bug.js` sets up an interval using `setInterval` but lacks a return function to clear the interval when the component unmounts.  This results in a continuously running interval, even after the component is removed from the DOM.

## Solution
The `bugSolution.js` file demonstrates the corrected code. The `useEffect` hook now includes a return function that uses `clearInterval` to clear the interval when the component unmounts, preventing the memory leak.