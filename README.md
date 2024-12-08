# React useEffect Hook Missing Dependency
This repository demonstrates a common bug in React applications: a missing dependency in the useEffect hook.  The bug causes unexpected behavior because the effect doesn't run when expected.

## The Bug
The `MyComponent` component uses `useState` to manage a count. The `useEffect` hook is intended to log a message when the count is greater than 0. However, the `count` variable is missing from the dependency array, which means that the effect will only run once, on mount. Subsequent changes to the count won't trigger the effect.

## The Solution
The solution is to include `count` in the dependency array. This ensures the effect runs whenever the `count` value changes.  The updated component now correctly logs the message when the count is greater than 0.

## How to reproduce the bug
1. Clone the repository
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs.  The message will only log once, on mount, and not when the count updates.

## How to fix the bug
1. Clone the repository
2. Run `npm install`
3. Run `npm start`
4. Compare the output to the fixed version in bugSolution.js
