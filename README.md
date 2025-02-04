# Expo Linking API: Unreliable Deep Link Handling

This repository demonstrates a common issue with the Expo Linking API, specifically concerning the unreliable handling of deep links, and provides a solution.

## Problem

The Expo Linking API, when used with universal links, may fail to open the app from a deep link or might open the wrong screen within the app. This is often caused by incorrect configuration or server-side problems.

## Solution

The provided solution involves verifying and correcting the following:

1. **Correct configuration of `app.json`:** Ensure that the `ios` and `android` sections have the correct settings for universal links.
2. **Server-side configuration:** Verify that the server correctly returns a `Link` header with the appropriate information for universal links.
3. **Handling of the `url` in the `Linking.addEventListener`:** Ensure your app correctly interprets the received `url` and navigates to the correct screen.
4. **Proper error handling:** Implement error handling to catch and resolve issues when opening links.

## How to use this example

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `npm install` to install the necessary packages.
4. Run `expo start` to start the development server.
5. Test deep linking with a universal link.