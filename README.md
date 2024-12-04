# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook. The bug arises from attempting to update state within the `useEffect`'s callback function using a value that depends on the current state, while including the state variable in the dependency array, creating a circular dependency and causing an infinite re-render loop.

## Bug Description

The `bug.js` file contains a component with a `useState` hook and an `useEffect` hook that tries to increment the state variable in each render, resulting in an infinite render loop because the dependency array includes the state variable itself.  This isn't always easy to spot. 

## Solution

The `bugSolution.js` file demonstrates the correct way to handle this.  Avoid including state variables that you modify in the `useEffect` in the dependency array.  Instead, use functional updates or other strategies to correctly manage state updates.
