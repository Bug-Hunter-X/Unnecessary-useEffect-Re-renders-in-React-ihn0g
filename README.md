# Unnecessary useEffect Re-renders in React

This repository demonstrates a common issue in React: an `useEffect` hook that runs more frequently than necessary.  The example shows how an effect with an incorrect dependency array leads to unnecessary re-renders and potential performance problems.

## Bug Description

The `useEffect` hook in the provided `MyComponent` runs after every render, including the initial render. This is because the dependency array is missing or incomplete, leading to an effect that runs on every state change, even if the state change does not affect the effect's logic.

## Solution

The correct dependency array should only include the state variables that the effect relies on. This ensures that the effect only runs when those specific variables change, which solves the issue of unnecessary re-renders.
