# React useEffect setInterval Memory Leak

This repository demonstrates a common mistake when using `setInterval` within the `useEffect` hook in React.  Failing to include a cleanup function leads to a memory leak, as the interval continues to run even after the component unmounts.

## The Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it lacks a cleanup function in the `useEffect` hook to stop the interval when the component is unmounted. This results in a memory leak.

## The Solution
The `bugSolution.js` file provides the corrected code.  A cleanup function is added to `useEffect` which uses `clearInterval` to stop the interval before the component unmounts, preventing the memory leak.

## How to Reproduce
1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server. Observe the count in the console and the browser.