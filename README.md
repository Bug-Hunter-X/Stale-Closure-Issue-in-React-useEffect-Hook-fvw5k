# Stale Closure Issue in React useEffect Hook
This repository demonstrates a common mistake when using the `useEffect` hook in React: creating a stale closure.  The example shows how an incorrect implementation can lead to unexpected behavior where the count is not updated correctly.

## Bug Description
The `useEffect` hook is used incorrectly, resulting in the `count` variable inside the effect not reflecting the most recent value. This is because the `count` is captured during the initial render and remains unchanged despite later updates, thus leading to a stale closure.

## Solution
The solution demonstrates the correct use of the `useEffect` hook.  By including the `count` variable in the dependency array, the effect re-runs whenever the count changes, ensuring that the latest value is used during logging.
