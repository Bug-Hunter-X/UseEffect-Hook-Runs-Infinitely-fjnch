# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications where the `useEffect` hook runs infinitely, leading to performance issues and console spam.  The bug stems from improper dependency management within the `useEffect` hook.

## Bug Description
The `useEffect` hook is designed to perform side effects after every render.  However, if the dependency array is missing or incorrectly specified, the effect will run repeatedly, creating an infinite loop. This example showcases a scenario where the effect runs even though the dependencies haven't changed, resulting in the component re-rendering itself constantly.

## Solution
The solution involves correctly specifying the dependencies array in the `useEffect` hook.  By only including `count` in the array, the effect only runs when the `count` variable changes, preventing the infinite loop.