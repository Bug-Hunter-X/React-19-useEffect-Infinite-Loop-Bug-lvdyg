# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common error in React 19 involving the `useEffect` hook and its dependency array.  The example shows an infinite loop caused by an incorrectly specified dependency array, leading to excessive re-renders and potential performance issues.

## Bug Description
The `useEffect` hook is used to perform side effects after a component renders.  The second argument of `useEffect` is the dependency array which determines when the effect should run.  If this array is incorrect or missing, it can lead to unintended behavior.

In this case, omitting `count` from the dependency array results in the effect executing after every render, causing a continuous loop because `setCount` triggers a re-render. 

## Solution
The solution involves correctly specifying the `count` variable in the dependency array. This ensures the effect runs only when the `count` value changes.