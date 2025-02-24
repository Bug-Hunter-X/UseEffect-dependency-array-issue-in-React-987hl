# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook related to the dependency array.  The provided code contains a logic flaw in how it handles changes in state, leading to unexpected behavior.  The solution demonstrates the correct way to manage dependencies within the `useEffect` hook.

## Bug Description:

The `MyComponent` uses `useEffect` to log a message whenever the `count` state variable changes. However, the condition `if (count !== 0)` within `useEffect` is incorrect.  It only triggers the log if `count` is not equal to 0, ignoring subsequent changes where `count` might be greater than 0.

## Solution:

The corrected `useEffect` does not include any condition to control logging. Instead, it relies on the dependency array `[count]` to trigger the effect whenever the `count` value changes, which is the correct way to handle updates within useEffect.