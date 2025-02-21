# React Native AsyncStorage Non-String Value Error

This repository demonstrates a common yet subtle bug in React Native when using AsyncStorage to store data. AsyncStorage only accepts strings; attempting to store other data types like objects or numbers silently fails, leading to unexpected app behavior.

## The Bug

The core issue is the lack of explicit error handling and informative error messages when storing non-string values in AsyncStorage.  This makes debugging difficult, as the error may manifest indirectly.

## The Solution

The solution involves robust error handling and type checking before storing data in AsyncStorage.  All data must be stringified before storage and parsed back to its original type after retrieval.  This ensures data integrity and provides better debugging capabilities.

## How to reproduce the bug

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run the app and observe the unexpected behavior.