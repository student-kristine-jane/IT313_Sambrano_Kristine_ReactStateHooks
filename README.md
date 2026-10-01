# IT313 React State and Hooks

## Problem

This project is a Lab Timer and Practice Tracker for students during laboratory sessions. It allows the user to track the number of practice problems solved and the amount of time spent working.

## Approach

The application uses React Native with Expo.

I used useState to manage the solved counter and the running state of the stopwatch.

I used useEffect inside a custom useStopwatch hook to create a timer that increases every second while the stopwatch is running.

The effect also has a cleanup function using clearInterval so the timer stops correctly when the stopwatch is stopped or the component is unmounted.

Conditional rendering is used to display "Great job!" when the solved count reaches five and to display either "Running..." or "Paused" depending on the stopwatch state.

The state is lifted to LabScreen so that PracticeTracker and Stopwatch can receive their required data through props.

## How to Run

1. Install Node.js and Expo.
2. Open the project folder in VS Code.
3. Open the terminal.
4. Run:

npx expo start

5. Scan the QR code using Expo Go.
6. Make sure the phone and computer are connected to the same network.

## Features

- Solve +1 counter
- Reset practice counter
- Start stopwatch
- Stop stopwatch
- Running and Paused status
- Great job message after five solved problems
- Stopwatch cleanup using clearInterval
- Custom useStopwatch hook
