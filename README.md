# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to incorrect dependency management within the `useEffect` function.

## Bug Description
The provided `MyComponent` utilizes the `useEffect` hook to log the render count and component unmount. However, the dependency array `[count]` is missing resulting in the effect running after every render and updating the count state which cause the infinite loop.

## Solution
The solution involves correctly specifying the dependency array in the `useEffect` hook to control when the effect runs. Only updating the state when necessary can avoid this bug.