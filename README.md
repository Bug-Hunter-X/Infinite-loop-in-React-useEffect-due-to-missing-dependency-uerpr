# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications: an infinite loop caused by a missing dependency in the `useEffect` hook.

## Bug Description
The `MyComponent` component uses `useState` to manage a count.  The `useEffect` hook logs the count to the console after every render. However, the `count` variable is missing from the dependency array. This causes the effect to run on every render, leading to an infinite loop and potentially crashing the browser.

## Bug Solution
The solution involves adding `count` to the dependency array of `useEffect`. This ensures that the effect only runs when the value of `count` changes.