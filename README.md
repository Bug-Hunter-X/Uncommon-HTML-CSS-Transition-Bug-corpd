# Uncommon HTML/CSS Transition Bug

This repository demonstrates a subtle bug related to CSS transitions in HTML.  The bug occurs when attempting to show a hidden element immediately after hiding it within the same function, preventing the transition effect from working as expected. The solution involves using `setTimeout` to introduce a slight delay before showing the element again.

## Bug Description:

A CSS transition is set up to smoothly animate the display property change of a div element.  However, when the JavaScript function attempts to hide and then immediately show the div, the transition is skipped, resulting in a jarring, abrupt change in visibility.

## Solution:
The solution leverages `setTimeout` to create a small delay (e.g., 0 milliseconds) between hiding and showing the element. This delay allows the browser to properly apply the transition effect before the visibility change is reversed.

## How to Reproduce:
1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Click the "Click Me" button.  Observe that the div disappears and reappears without any transition.
4. Open `bugSolution.html`. Notice the smooth transition when clicking the button. 
