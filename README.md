# Unexpected Element Removal When Setting innerHTML to null
This repository demonstrates an uncommon HTML bug related to setting the innerHTML property to null.  When a developer sets the innerHTML property of an element to null, one might expect the element's content to be cleared, leaving an empty element. However, in many browsers, this results in the complete removal of the element from the DOM. This is a subtle error that's easily missed during development and testing.

## Bug Description
Setting innerHTML to null unexpectedly removes the element instead of clearing its content.

## How to reproduce the bug
1. Clone the repository.
2. Open `bug.html` in your web browser.
3. Observe that the div element with the id "myDiv" disappears completely.  The expected behavior would be for the div to remain, but its contents to be empty.

## Solution
The solution involves using an empty string '' instead of null to clear the innerHTML of the element. This correctly leaves the element in place while removing its content.
