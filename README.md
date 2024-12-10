# React Native Dimensions API Inconsistency on Android

This repository demonstrates a common issue with the `Dimensions` API in React Native on Android. The `Dimensions.get('window')` method may return outdated or inaccurate screen dimensions, causing UI layout problems.

The `DimensionsBug.js` file shows how the issue manifests. The `DimensionsBugSolution.js` file offers a solution using `Dimensions.addEventListener` for more reliable dimension updates.

## How to Reproduce

1. Clone this repository.
2. Run the app on an Android device or emulator.
3. Rotate the device.
4. Observe that the UI might not resize correctly, indicating that the `Dimensions` API returned incorrect values.

## Solution

Use `Dimensions.addEventListener` to listen for dimension changes and update the UI accordingly instead of relying on a single call to `Dimensions.get('window')`. See `DimensionsBugSolution.js` for an example.