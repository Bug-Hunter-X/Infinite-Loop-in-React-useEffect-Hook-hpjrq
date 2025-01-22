# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The `useEffect` hook, when used incorrectly without specifying dependencies, can lead to infinite loops and unexpected behavior.

The bug occurs when the `useEffect` function attempts to update the state it depends on without listing that state in the dependency array. This creates a cycle where the state update triggers a re-render, which triggers the `useEffect` again, leading to continuous updates.

The solution involves correctly specifying the dependencies in the `useEffect` dependency array, ensuring that the effect runs only when necessary.

## How to reproduce

1. Clone the repository
2. Run `npm install`
3. Run `npm start`

Observe the infinite loop in the console and the continuously updating counter.

## Solution

The solution is provided in `bugSolution.js`.