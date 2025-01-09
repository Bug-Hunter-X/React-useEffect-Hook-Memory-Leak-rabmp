# React useEffect Hook Memory Leak

This repository demonstrates a common error in React applications involving the `useEffect` hook: forgetting the return statement for cleanup functions.

The `bug.js` file shows the problematic code where a `console.log` is used within `useEffect` without a return statement. This can lead to memory leaks when the component unmounts, as any timers, event listeners, or subscriptions started within the effect won't be properly cleaned up. 

The `bugSolution.js` demonstrates the correct usage of `useEffect` by including a return statement, ensuring proper cleanup during component unmounting. 