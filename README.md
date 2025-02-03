# React useEffect Infinite Loop Bug

This repository demonstrates a common mistake when using the `useEffect` hook in React: forgetting to include all relevant variables in the dependency array. This leads to an infinite loop because the effect runs continuously.

The `bug.js` file contains the buggy code. The `bugSolution.js` file shows the corrected version.

## Bug

The original code has an infinite loop because the `count` variable is not included in the dependency array of `useEffect`.  This means the effect is triggered after every render, causing `count` to update infinitely.

## Solution

The solution involves including `count` in the dependency array, ensuring that the effect only runs when `count` changes.