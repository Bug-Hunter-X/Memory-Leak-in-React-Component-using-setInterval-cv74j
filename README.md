# React setInterval Memory Leak
This repository demonstrates a common error in React components: using `setInterval` within `useEffect` without a cleanup function. This leads to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it lacks a cleanup function to clear the interval when the component unmounts. This causes the interval to continue running even after the component is removed from the DOM, leading to a memory leak.

## Solution
The `bugSolution.js` file demonstrates the correct way to use `setInterval` in a React component. It includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts. This prevents memory leaks and ensures the component behaves as expected.

## How to reproduce
1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the behavior of the component in both `bug.js` and `bugSolution.js`.