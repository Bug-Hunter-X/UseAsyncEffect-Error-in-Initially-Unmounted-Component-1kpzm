# Expo useAsyncEffect Error in Initially Unmounted Component

This repository demonstrates a bug encountered when using Expo's `useAsyncEffect` hook within a component that isn't rendered initially.  The issue arises because `useAsyncEffect` attempts asynchronous operations before the component mounts, leading to errors from accessing undefined props.

The `bug.js` file shows the problematic code, resulting in an error. The solution in `bugSolution.js` addresses the issue by conditionally executing the asynchronous operation only after the component is mounted and the necessary props are available.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `expo start`.
5. Observe the error in the console (bug.js).  Then switch to the solved version (bugSolution.js) to see the corrected behavior.

## Solution

The solution involves checking if the necessary props are defined before executing the asynchronous operation within `useAsyncEffect`.  This ensures the operation only runs after the component has successfully mounted and received its props.  Refer to `bugSolution.js` for a working implementation.