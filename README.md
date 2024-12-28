# Incorrect State Update in React's useEffect Hook

This repository demonstrates a common error in React applications involving the `useEffect` and `useState` hooks. The issue arises from not properly handling state updates within the `useEffect` hook when using `setInterval`.

The problem lies in directly accessing the `count` variable within the `setInterval` callback. By the time the callback executes, the value of `count` might have already changed, leading to stale closures and incorrect updates.

The solution involves using a functional update to ensure that the `setCount` function always uses the latest state value.