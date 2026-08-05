# Daymark

Daymark is a small, mobile-friendly web app for calculating daily work hours. It runs entirely in the browser and requires no build step, framework, or external dependency.

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

## Theme preference

Use the theme selector in the header to choose **System**, **Light**, or **Dark**. System follows the operating system setting. Light and Dark overrides are saved for one year in the `daymark-theme` cookie. Selecting System removes that cookie.


## Privacy
All calculations happen locally in the browser. Daymark does not send or store time-entry data.
