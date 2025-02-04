# ConcurrentModificationException in Kotlin MutableMap removeIf

This repository demonstrates a subtle bug related to the `removeIf` function in Kotlin when used with `MutableMap`.  While `removeIf` works correctly with `MutableList` and `MutableSet`, it throws a `ConcurrentModificationException` when used with a `MutableMap`.

The issue stems from the fact that iterating and modifying a map concurrently using `removeIf` is not safe. The `removeIf` function modifies the map while iterating, leading to the exception.

## Solution

The provided solution demonstrates using an iterator to safely remove elements from a `MutableMap`.

## Usage

1. Clone this repository.
2. Open the project in your IDE.
3. Run the provided `bug.kt` and `bugSolution.kt` files.

This will showcase the error and the correct way to remove elements from a `MutableMap` using an iterator.