# React UseEffect setInterval Memory Leak
This repository demonstrates a common error in React applications: using `setInterval` within a `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

## Bug Description
The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak. The interval continues to run even after the component is no longer rendered.

## Solution
The solution involves using the return function of the `useEffect` hook to clear the interval before the component unmounts.  This ensures that the interval is properly stopped, preventing the memory leak.  See `bugSolution.js` for the corrected code.