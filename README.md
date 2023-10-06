<h1 align="center">Javascript Dom CheatSheet:)</h1>

[//]: # (Table of Content)
<a name="top"></a>

## Table Of Contents 🙋‍♂️ content

> Click on any topic to go there

1. [Selecting Elements](#selecting-elements)
2. [Manipulating Elements](#manipulating-elements)
3. [Creating Elements](#creating-elements)
4. [Modifying the DOM](#modifying-the-dom)
5. [Event Handling](#event-handling)
6. [Common DOM Events](#common-dom-events)
7. [Traversing the DOM](#traversing-the-dom)
8. [Element insertAdjacentElement Method](element-insertadjacentelement-method)
9. [Window and Document Properties](#window-and-document-properties)
10. [Form Handling](#form-handling)
11. [AJAX (Asynchronous JavaScript and XML)](#ajax-asynchronous-javascript-and-xml)
12. [Local Storage](#local-storage)
13. [DOM Manipulation Best Practices](#dom-manipulation-best-practices)
14. [Learning Resources](#learning-resources)

---

## Selecting Elements

1. `document.getElementById(id)` - Selects an element by its ID.
2. `document.getElementsByClassName(className)` - Selects elements by their class name.
3. `document.getElementsByTagName(tagName)` - Selects elements by their HTML tag name.
4. `document.querySelector(selector)` - Selects the first matching element by a CSS selector.
5. `document.querySelectorAll(selector)` - Selects all matching elements by a CSS selector.

   **Learning Resources:**
   - [MDN Web Docs: Document.querySelector](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector)
   - [MDN Web Docs: Document.querySelectorAll](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll)

---

#### [Go to top:arrow_up: ](#top)

## Manipulating Elements

1. `element.innerHTML` - Gets or sets the HTML content of an element.
2. `element.textContent` - Gets or sets the text content of an element.
3. `element.setAttribute(attribute, value)` - Sets an attribute on an element.
4. `element.getAttribute(attribute)` - Gets the value of an attribute.
5. `element.style.property = value` - Changes the inline CSS style of an element.
6. `element.classList.add(className)` - Adds a CSS class to an element.
7. `element.classList.remove(className)` - Removes a CSS class from an element.
8. `element.classList.toggle(className)` - Toggles the presence of a CSS class on an element.

   **Learning Resources:**
   - [MDN Web Docs: Element.innerHTML](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)
   - [MDN Web Docs: Element.textContent](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent)
   - [MDN Web Docs: Element.setAttribute](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute)
   - [MDN Web Docs: Element.style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style)
   - [MDN Web Docs: Element.classList](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)

---

#### [Go to top:arrow_up: ](#top)

## Creating Elements

1. `document.createElement(tagName)` - Creates a new element.
2. `document.createTextNode(text)` - Creates a new text node.

   **Learning Resources:**
   - [MDN Web Docs: document.createElement](https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement)
   - [MDN Web Docs: document.createTextNode](https://developer.mozilla.org/en-US/docs/Web/API/Document/createTextNode)

---

#### [Go to top:arrow_up: ](#top)

## Modifying the DOM

1. `parent.appendChild(child)` - Appends a child element to a parent element.
2. `parent.removeChild(child)` - Removes a child element from a parent element.
3. `element.parentNode` - Gets the parent node of an element.
4. `element.nextSibling` - Gets the next sibling node of an element.
5. `element.previousSibling` - Gets the previous sibling node of an element.

   **Learning Resources:**
   - [MDN Web Docs: Node.appendChild](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild)
   - [MDN Web Docs: Node.removeChild](https://developer.mozilla.org/en-US/docs/Web/API/Node/removeChild)

---

#### [Go to top:arrow_up: ](#top)

## Event Handling

1. `element.addEventListener(event, callback)` - Attaches an event listener to an element.
2. `element.removeEventListener(event, callback)` - Removes an event listener from an element.
3. Event Object Properties (e.g., `event.target`, `event.preventDefault()`, `event.stopPropagation()`)

   **Learning Resources:**
   - [MDN Web Docs: addEventListener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
   - [MDN Web Docs: Event](https://developer.mozilla.org/en-US/docs/Web/API/Event)
   - [MDN Web Docs: Event.preventDefault](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault)
   - [MDN Web Docs: Event.stopPropagation](https://developer.mozilla.org/en-US/docs/Web/API/Event/stopPropagation)

---

#### [Go to top:arrow_up: ](#top)

## Common DOM Events

- `click`
- `submit`
- `mouseover`
- `keydown`
- `load`
- `DOMContentLoaded`

---

#### [Go to top:arrow_up: ](#top)

## Traversing the DOM

- `element.childNodes` - Gets a collection of child nodes.
- `element.firstChild` - Gets the first child node.
- `element.lastChild` - Gets the last child node.
- `element.parentElement` - Gets the parent element.
- `element.nextElementSibling` - Gets the next sibling element.
- `element.previousElementSibling` - Gets the previous sibling element.

---

#### [Go to top:arrow_up: ](#top)


## Element insertAdjacentElement method

- `element.insertAdjacentElement(position, element)` - Inserts an element into the specified position relative to the current element.

   - `position` can be one of the following values:
     - `"beforebegin"`: Inserts the element as a previous sibling.
     - `"afterbegin"`: Inserts the element as the first child.
     - `"beforeend"`: Inserts the element as the last child.
     - `"afterend"`: Inserts the element as a subsequent sibling.
     
   - `element` is the element to be inserted.

   **Example:**
   ```javascript
   const parentElement = document.getElementById("parent");
   const newElement = document.createElement("div");
   newElement.textContent = "New Element";
   
   // Insert newElement as the first child of parentElement
   parentElement.insertAdjacentElement("afterbegin", newElement);
   ```

   **Learning Resources:**
   - [MDN Web Docs: Element.insertAdjacentElement](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentElement)


#### [Go to top:arrow_up: ](#top)


## Window and Document Properties

- `window.innerWidth` / `window.innerHeight` - Gets the inner width and height of the window.
- `window.scrollX` / `window.scrollY` - Gets the horizontal and vertical scroll positions.
- `document.title` - Gets or sets the document's title.
- `document.URL` - Gets the URL of the document.

---

## Form Handling

- `form.submit()` - Submits a form.
- `input.value` - Gets or sets the value of an input element.
- `input.checked` - Gets or sets the checked state of a checkbox or radio button.
- `input.focus()` - Gives focus to an input element.
- `input.blur()` - Removes focus from an input element.

---

#### [Go to top:arrow_up: ](#top)

## AJAX (Asynchronous JavaScript and XML)

- `XMLHttpRequest` object - Used for making HTTP requests.
- `fetch` API - A modern alternative for making HTTP requests.
- `Promise` API for asynchronous operations - Used for handling asynchronous tasks.

---

## Local Storage

- `localStorage.setItem(key, value)` - Stores a value in local storage.
- `localStorage.getItem(key)` - Retrieves a value from local storage.
- `localStorage.removeItem(key)` - Removes a value from local storage.
- `localStorage.clear()` - Clears all data from local storage.

---

#### [Go to top:arrow_up: ](#top)

## DOM Manipulation Best Practices

- Minimize DOM manipulation for better performance.
- Use event delegation for efficient event handling.
- Cache DOM elements to avoid redundant lookups.
- Use `textContent` over `innerHTML` when dealing with text content to prevent security risks (XSS attacks).

---

## Learning Resources

- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API) - Comprehensive documentation on the DOM and JavaScript.
- [W3Schools DOM Tutorial](https://www.w3schools.com/js/js_htmldom_methods.asp)
- [Javascript Tutorial Sit Javascript DOM](https://www.javascripttutorial.net/javascript-dom/)
- [Tutorial Repblic Javascript DOM](https://www.tutorialrepublic.com/javascript-tutorial/javascript-dom-nodes.php)

#### [Go to top:arrow_up: ](#top)
