# Uncommon CSS Specificity Bug: Unexpected Style Override

This repository demonstrates a subtle CSS bug related to specificity and the order of styles in a stylesheet.  The problem arises from the interaction between nested selectors and the cascading nature of CSS.  A less specific selector, when placed after a more specific selector, unexpectedly overrides the latter due to the order of declarations.

## Bug Description
The provided `bug.css` file contains a CSS stylesheet with nested selectors.  The expectation is that the nested selector `.container .inner` should apply a light green background color to the inner element within a container. However, due to the placement of the `.inner` selector and the cascading behavior of CSS, the `.inner` selector's lightcoral background color takes precedence, resulting in an unexpected visual output.

## Solution
The `bugSolution.css` file provides a corrected version of the stylesheet.  The solution rearranges the selectors to ensure that the more specific selector `.container .inner` always takes precedence. Alternatively, the selector specificity is enhanced by adding another selector to the `.inner` selector to reduce ambiguity and enhance the specificity of the intended selector.