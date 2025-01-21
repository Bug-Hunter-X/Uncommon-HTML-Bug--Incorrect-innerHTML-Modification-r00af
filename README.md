# Uncommon HTML Bug: Premature innerHTML Modification

This repository demonstrates an uncommon bug related to modifying an element's `innerHTML` property before the element is fully parsed and added to the Document Object Model (DOM).  This is different from common syntax errors; it's a timing issue.

## Bug Description

The `bug.html` file attempts to change the `innerHTML` of a div element before the div element itself exists in the DOM. This results in a runtime error if the browser strictly enforces the condition or could fail silently otherwise. 

## Solution

The `bugSolution.html` file demonstrates two ways to avoid the issue:

1. **Event Listener:**  Using an event listener to ensure the `innerHTML` is updated only after the DOMContentLoaded event, signifying the completion of the DOM parsing process. 
2. **Conditional Check:**Checking the existence of the element before trying to access its properties.

This subtle timing-related error highlights the importance of understanding DOM loading and using appropriate event handling mechanisms or conditional checks when manipulating the DOM.