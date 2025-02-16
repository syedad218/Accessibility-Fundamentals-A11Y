# Accessibility-a11y-

### Accessibility Tree

- Accessibility tree is a subset of the DOM tree, that are used by assistive technologies such as screen readers to provide information about the nodes in the DOM tree to users with disabilities.
- When we use the right semantic HTML elements, the browser automatically creates an accessibility tree for us. This is why it is important to use the right semantic HTML elements when building a website.
- Chrome DevTools has a feature that allows you to inspect the accessibility tree of a webpage. You can access this feature by opening the Chrome DevTools, clicking on the "Elements" tab, and then clicking on the "Accessibility" tab. Enable full page accessibility to see the full accessibility tree of the webpage.

<b>Other tools that can be used to test the accessibility of a webpage include:</b>

- Lighthouse
- Axe
- Accessibility Inspector
- Contrast Checker
- AI assistance tools

### Accessibility Guidelines (Web Content Accessibility Guidelines 2.0)

- Levels of conformance: A, AA, AAA: A is the lowest level of conformance, while AAA is the highest level of conformance.
- Text Contrast:
  - AA: 4.5:1 for normal text, 3:1 for large text <i>( >= 24px )</i>
  - AAA: 7:1 for normal text, 4.5:1 for large text
  - Tools: Contrast Checker and Inspect Element in Chrome DevTools
- Color:
  - Ensure that color is not the only visual means of conveying information
- Alternative Text for Images:
  - Always provide alternative text for images using the alt attribute
  - For decorative images, use an empty alt attribute (alt="")
- Links:
  - Use \<a> tags for links, should be recognizable and have a non-ambiguous text, understandable out of context
  - Nested content inside Links is not recommended as it can be confusing for screen readers, instead use advanced CSS techniques to make whole block clickable and place the link inside the block with a proper aria-label
- Labels:
  - Use \<label> tags for form elements, and ensure that the label is associated with the form element using the for attribute using the id of the form element.
  - Placeholder attribute is not a substitute for a label
  - Placeholder should be used to provide an example of the type of input that is expected
  - text inside buttons and links acts as a label, if we use a non semantic element like a div, we can use aria-label to provide a label for buttons and links and a tabindex attribute to provide it with keyboard accessibility
- Radio Buttons and Checkboxes:
  - Use \<fieldset> and \<legend> tags to group radio buttons and checkboxes together
- Semantic HTML:
  - Search engines and screen readers rely on semantic HTML to understand the structure of a webpage
  - Landmark regions: \<header>, \<nav>, \<main>, \<footer>, \<section>
- Lists:
  - Use \<ul> for unordered lists, \<ol> for ordered lists for connected consecutive items
  - Use \<li> for list items
- Font Size:
  - Use relative units like em, rem, %, vw, vh for font sizes
  - Default settings
    - 1em = 16px
    - 1.5rem = 24px
    - 2rem = 32px
- Headings:
  - Use \<h1> to \<h6> tags for headings, and ensure that the headings are used in consecutive order
  - Only use one \<h1> tag per page and don't skip heading levels
  - Apply them for structure, not for styling
- Aria (Accessible Rich Internet Applications):
    - Aria attributes should only be used when there is no native HTML element that can be used to provide the same information
    - Aria attributes should be used sparingly and only when necessary
    - Aria attributes should be used to provide additional information, not to change the default behavior of HTML elements
- Aria Live Regions:
    - Aria-live attribute is used to define a live region for content that changes dynamically like notifications, alerts, and errors
    - Settings:
        - aria-live="off" - Default value, no live updates
        - aria-live="polite" - Updates are announced when the user is idle
        - aria-live="assertive" - Updates are announced immediately
    - Aria-live regions are used to announce changes to screen readers
    - Aria-live regions should be used sparingly and only when necessary
- Skip Navigations Link:
    - Skip navigation links are used to allow users to skip repetitive content and navigate directly to the main content of a webpage
    - Skip navigation links are hidden from view until they receive focus
    - Skip navigation links are used to improve keyboard accessibility
    - Add a transition effect to make it identifiable when it receives focus and to avoid skipping it accidentally
    - Accessible settings:
        - opacity: 0
        - left: 100%
        - transform: translateX(100%);
        - position: absolute
