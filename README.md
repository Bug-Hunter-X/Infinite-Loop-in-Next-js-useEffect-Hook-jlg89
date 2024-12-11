# Next.js useEffect Infinite Loop Bug

This repository demonstrates a common bug in Next.js applications involving the `useEffect` hook.  The bug is caused by a missing dependency in the `useEffect`'s dependency array, leading to an infinite loop.

## Bug Description

The `MyComponent` component uses `useState` to track a count. The `useEffect` hook logs the count to the console.  However, because a dependency is incorrectly omitted, the effect runs repeatedly, causing the counter to increment infinitely and potentially crashing the application.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Observe the rapidly incrementing counter in the browser's console and the UI. 

## Solution

The solution involves adding the `count` variable to the dependency array of `useEffect`, ensuring it only runs when the `count` value changes.