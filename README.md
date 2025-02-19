# React Native FlatList Performance Issue: Missing or Incorrect `keyExtractor`

This repository demonstrates a common performance issue in React Native's FlatList component caused by an incorrectly implemented or missing `keyExtractor` prop.  When working with large datasets, using a proper `keyExtractor` is crucial for optimal performance.

The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version using a proper `keyExtractor`.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app on either Android or iOS.
4. Observe the performance difference between the buggy and fixed versions.

## Problem

The `bug.js` demonstrates a FlatList without a `keyExtractor` or with an inefficient one. This leads to unnecessary re-renders causing lag and potential crashes, especially with larger datasets.

## Solution

The `bugSolution.js` file shows how to fix the problem by providing a `keyExtractor` function that returns a unique and stable identifier for each item in the data array.  It's vital that this identifier remains constant for each data item, even if other item properties may change.