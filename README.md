# React useState Hook Not Updating UI with Object State

This repository demonstrates a common but subtle bug in React's `useState` hook. When updating an object or array within the state, React's shallow comparison might not detect the change if a new object is created instead of directly mutating the original object.  This results in the UI not reflecting the changes in state.

## Problem
The provided `bug.js` file shows an example where incrementing a value within an object using `useState` fails to update the UI.  The issue is that `setCount` creates a new object, and React's comparison detects no difference between the old and new object (due to shallow comparison), preventing the re-render.

## Solution
The `bugSolution.js` file demonstrates how to correctly handle object updates by creating a new object with the spread operator or functional update. This forces React to detect a change and update the UI accordingly.  This approach helps avoid unintended mutations and ensures correct state updates.

## How to Run
1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.