# Daymark

Daymark is a small, mobile-friendly, mostly vibe-coded web app for calculating daily work hours. It runs entirely in the browser and requires no build step, framework, or external dependency.

## Features

- Calculate hours worked from a start time, end time, lunch, and optional breaks.
- Display worked time as decimal hours.
- Calculate when to stop working from a start time, desired hours, and breaks.
- Handle shifts and calculated stop times that cross midnight.
- Add or remove optional breaks independently on either calculator.
- Follow the operating system's light or dark theme by default.
- Save a Light or Dark theme override in a browser cookie.
- Support desktop and mobile screen sizes, touch input, and keyboard tab navigation.

## Using the app

Open `index.html` in a modern browser. For the most consistent cookie behavior, serve the repository directory with any local static web server and open the URL it provides.

Both calculators update automatically when an input changes. Lunch defaults to 30 minutes, and desired work time defaults to 8 hours.

Breaks must be whole minutes from 0 to 1440, with a combined maximum of 24 hours. Desired work time accepts tenths of an hour from 0.1 to 24 hours. Incomplete or invalid entries clear the result until corrected. Screen-reader feedback is announced when an edit is committed or the Calculate button is pressed.

The default view is designed to fit portrait phone viewports as small as 320 × 520 CSS pixels, including both calculator tabs. Short viewports omit the introductory sentence to preserve room for the controls. Extra breaks, validation messages, enlarged text, and the on-screen keyboard may require scrolling.

## Theme preference

Use the theme selector in the header to choose **System**, **Light**, or **Dark**. System follows the operating system setting. Light and Dark overrides are saved for one year in the `daymark-theme` cookie. Selecting System removes that cookie.


## Privacy
All calculations happen locally in the browser. Daymark does not send or store time-entry data.

## Regression checks

With Node.js 22 or later and Chrome or Edge installed, run `node tests/check-ui.mjs`. The checks use a temporary browser profile and cover mobile and desktop layout, input validation, overnight calculations, keyboard focus, live announcements, and action-text contrast. No npm packages are needed. Set `DAYMARK_BROWSER` to a Chromium executable if it is not detected automatically.

Use `node tests/check-ui.mjs --screenshots` to retain sample screenshots in the temporary test directory for visual review.
