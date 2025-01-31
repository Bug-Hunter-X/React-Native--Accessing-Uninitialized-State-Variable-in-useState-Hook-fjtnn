# React Native: Accessing Uninitialized State Variable

This repository demonstrates a common error in React Native applications: accessing a state variable before it has been initialized using the `useState` hook.  The example shows how this can lead to unexpected behavior or crashes.

## Problem

The problem occurs because React's state updates are asynchronous.  When the component initially renders, the state variable might still be undefined, leading to errors if you try to access it before the state update completes.

## Solution

The solution is to conditionally render content only after the state variable has been initialized.  This can be done using optional chaining or the nullish coalescing operator.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` (or the iOS equivalent).
4. Observe the error message in the console and the unexpected behavior in the app.