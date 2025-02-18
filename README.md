# Uncommon HTML Bug: Handling Non-Existent Elements

This repository demonstrates a subtle error that can occur in HTML/JavaScript when attempting to manipulate the `innerHTML` property of an element that doesn't exist.  Failure to handle this properly can lead to silent errors and unexpected behavior.

The `bug.html` file contains the problematic code, while `bugSolution.html` presents a robust and safer approach.

The primary issue is the use of `document.getElementById()` without a check to ensure the element exists.  If the element is missing, accessing its `innerHTML` property in many browsers will throw a silent error, leading to unexpected behavior or a crash.

The solution showcases the importance of always checking for `null` when working with elements retrieved from `document.getElementById()`.  This prevents such errors and makes the code more resilient.