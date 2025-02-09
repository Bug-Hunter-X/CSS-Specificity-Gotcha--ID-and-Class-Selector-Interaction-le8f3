# CSS Specificity Gotcha: Unexpected Behavior with ID and Class Selectors

This repository demonstrates an uncommon CSS specificity issue that can lead to unexpected styling behavior. The problem involves the interaction between ID selectors and class selectors, particularly when nested elements are involved.

## The Issue

The core problem lies in how CSS resolves specificity when dealing with combinations of ID, class, and element selectors.  The rule `.container #myDiv` demonstrates this. Even though `#myDiv.container` seems more specific because it directly targets an element with both an ID and a class, `.container #myDiv` actually wins due to the higher specificity of the ID selector.

## How to reproduce
1. Clone this repository.
2. Open `bug.css` and `bugSolution.css` to observe the issue and solution.
3. Create an HTML file with the necessary divs and classes to test.

## Solution
The solution involves a careful understanding of CSS specificity and either adjusting selectors or making the intended styles more specific.