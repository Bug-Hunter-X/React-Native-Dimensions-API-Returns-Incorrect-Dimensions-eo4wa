# React Native Dimensions API Returns Incorrect Dimensions

This repository demonstrates a common bug in React Native where the `Dimensions` API returns incorrect or zero dimensions when accessed too early in a component's lifecycle.  The bug is reproduced in `DimensionsBug.js`, and a solution is provided in `DimensionsBugSolution.js`.

## Bug Description:

The `Dimensions` API, when accessed within `componentDidMount` or similar lifecycle methods, sometimes returns incorrect dimensions (often 0) before the layout has completed.  This leads to issues with element positioning, sizing, and calculations that depend on screen dimensions.

## Solution:

The solution involves using the `Layout` component or a similar approach to ensure that the dimensions are accessed after the layout is complete.  This prevents accessing the API before the layout has finalized.