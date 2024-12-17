# React 18+ useEffect Missing Dependency Warning

This repository demonstrates a common error in React 18+ related to the `useEffect` hook and missing dependencies, specifically when using `setInterval`.

## Problem
The `bug.js` file contains a component that uses `setInterval` within a `useEffect` hook without including `setInterval` in the dependency array. This leads to a warning in React 18+ and potentially unexpected behavior because the interval is not cleaned up correctly when the component unmounts.

## Solution
The `bugSolution.js` file shows the corrected implementation. By including an empty dependency array `[]`  it will only run the effect after mounting and the cleanup function ensures the interval is cleared when the component unmounts, preventing memory leaks.