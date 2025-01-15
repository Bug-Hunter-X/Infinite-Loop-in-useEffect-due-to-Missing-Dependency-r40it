# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by omitting a necessary dependency from the dependency array.

## The Bug
The `bug.js` file contains a component with a `useEffect` hook that logs the current count.  The problem is that the `count` variable is not included in the dependency array.  This means the effect runs after every render, even if the `count` value hasn't changed, leading to an infinite render loop and console spam.

## The Solution
The `bugSolution.js` file shows the corrected version. By adding `count` to the dependency array, the effect only runs when the value of `count` changes.