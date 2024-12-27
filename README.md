# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The example shows an infinite loop caused by improperly managing dependencies within the `useEffect` hook.

## Bug Description

The `useEffect` hook is used to perform side effects, such as data fetching or DOM manipulation, after a component renders.  However, if the dependencies array (the second argument to `useEffect`) is missing or incorrect, it can lead to unexpected behavior, including infinite loops.

In this specific case, the `useEffect` hook is updating the `count` state variable in every render cycle, creating an infinite loop because the effect runs continuously without any condition to stop it.

## Solution

The solution involves correctly defining the dependencies array.  In this case, the correct dependency should be the `count` state variable. If you do not add any dependencies then the effect will run only once after the initial render.