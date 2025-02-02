# React Native useRef Hook Object Persistence Issue

This repository demonstrates a common yet subtle bug in React Native when using the `useRef` hook with object initial values. The problem stems from the fact that re-renders cause useRef's object to be replaced, even if the underlying data isn't altered, making persistent updates challenging.  The provided solutions illustrate best practices for handling this issue.

## Bug Description
When an object is passed as the initial value to `useRef`, each component re-render replaces the object.  Modifying the object's properties within the component does not reflect these changes persistently. This can lead to unexpected behavior and potentially difficult-to-debug issues.

## Solution
Use functional updates to ensure that useRef modifies the existing object in place instead of replacing it with a new one.