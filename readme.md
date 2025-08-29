1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

Answer:

getElementById(id) returns a single element with the specified unique ID. Since IDs should be unique in an HTML document, this method returns just one element or null if none is found.

getElementsByClassName(className) returns a live HTMLCollection of all elements with the given class name. It can return multiple elements because many elements can share the same class.

querySelector(selector) returns the first element that matches a given CSS selector string.

querySelectorAll(selector) returns a static NodeList of all elements matching the CSS selector.

2. How do you create and insert a new element into the DOM?

Answer:

Use document.createElement(tagName) to create a new element (for example, document.createElement("div")).

To insert it into the DOM, use methods like parentElement.appendChild(newElement) to append it as the last child, or parentElement.insertBefore(newElement, referenceElement) to insert it before a specific child.

3. What is Event Bubbling and how does it work?

Answer:
Event Bubbling is the process where an event triggered on a child element propagates upward through its ancestors in the DOM tree, from the target element up to the root (document). For example, if you click a button inside a <div>, the click event first fires on the button (target), then bubbles up to the <div>, and then further up to parent elements, allowing multiple event handlers on ancestor elements to react.

4. What is Event Delegation in JavaScript? Why is it useful?

Answer:
Event Delegation leverages event bubbling by attaching a single event listener to a parent element instead of many listeners on individual child elements. When events bubble up, the parent can detect events on its children and handle them efficiently. This reduces the number of event listeners, improves performance, and allows dynamic handling of elements added after the event listener is attached.

5. What is the difference between preventDefault() and stopPropagation() methods?

Answer:

preventDefault() stops the browser from executing the element’s default action (e.g., preventing a form submission or a link navigation).

stopPropagation() stops the event from bubbling (or capturing) further — meaning no further event handlers on ancestor (or descendant, during capture) elements will be invoked for that event.