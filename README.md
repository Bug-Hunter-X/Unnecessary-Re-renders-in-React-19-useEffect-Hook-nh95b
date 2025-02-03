# Unnecessary Re-renders in React 19 useEffect Hook

This repository demonstrates a common issue in React 19 where the `useEffect` hook causes unnecessary re-renders, leading to performance problems.  The example shows how to identify and fix this problem by correctly specifying the dependency array.

## Problem:

The original `MyComponent` uses `useEffect` without properly specifying the dependency array, resulting in the effect running after *every* render, not just when `count` changes.  This leads to excessive logging and potential performance issues, especially in more complex applications.

## Solution:

The improved version (`bugSolution.js`) correctly specifies `[count]` as the dependency array, meaning the effect only runs when the `count` state variable changes.