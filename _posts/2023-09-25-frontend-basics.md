---
layout: "post"
title: "Web Frontend Basics: A Beginner's Guide"
---

Welcome to this guide on Web Frontend Basics. By the end of this post, you should have a solid grasp of foundational frontend concepts and be able to tackle common questions in the domain.

### 1. **RxJS and Observables**:
- **Observable**: Represents the idea of an invokable collection of future values or events.

```javascript
// Creating an observable
const observable = new Observable(subscriber => {
  subscriber.next('Hello');
  subscriber.next('World');
});

// Subscribing to an observable
observable.subscribe(val => console.log(val));
```
This code initializes an observable that emits the words "Hello" and "World". The `subscribe` function is used to listen to these emitted values.




- **BehaviorSubject**: A type of subject, a subject is both an Observable and an Observer. The BehaviorSubject stores the latest value emitted to its consumers and is stateful.

```javascript
// Using BehaviorSubject
const subject = new BehaviorSubject(0); // initial value

subject.subscribe({
  next: (v) => console.log(`observerA: ${v}`)
});

subject.next(1);
subject.next(2);
```
In this example, `subject` is a BehaviorSubject initialized with the value `0`. When we call `next(1)`, the value `1` is broadcasted to all subscribers.



### 2. **DOM Events**:
The DOM (Document Object Model) provides a structured representation of the web page. Events are actions that can be detected by JavaScript, like when an element gets focus.

### 3. **CSS Styling**:
**Positioning**: The `absolute` positioning allows you to set the position of an element relative to the nearest positioned ancestor.
**Text alignment**: The `justify` property aligns text to the full width of the container.

```css
/* Absolute Positioning */
.positioned-element {
    position: absolute;
    top: 50px;
    left: 50px;
}

/* Text Alignment */
.justified-text {
    text-align: justify;
}
```
The `positioned-element` class showcases how absolute positioning works, setting an element's position relative to its nearest positioned ancestor. The `justified-text` class aligns the text to the full width of its container.



### 4. **JavaScript Basics**:
- **Event Handlers**: Functions that handle events when they occur. Use the `this` keyword inside an event handler to refer to the element that received the event.
- **JSON**: JavaScript Object Notation, a lightweight data interchange format. Use `JSON.parse()` to convert a JSON string into a JavaScript object.

```javascript
// Event Handler with 'this'
button.addEventListener('click', function() {
  console.log(this);  // Refers to the button element
});

// Parsing a JSON string
const jsonString = '{"name":"John", "age":30, "city":"New York"}';
const obj = JSON.parse(jsonString);
console.log(obj.name);  // Outputs: John
```
The first code snippet demonstrates using the `this` keyword in an event listener. In this context, `this` refers to the DOM element that triggered the event. The second snippet showcases how to parse a JSON string into a JavaScript object.


### 5. **Web API and AJAX**:
RESTful services follow standard conventions for CRUD operations. 
- **HTTP Methods**: GET, POST, PUT, DELETE, etc.
- **Headers**: They provide meta-information about the request or response. The Content-Type header indicates the media type of the resource or data.

### 6. **Data Structures in Web Development**:
**Stack**: A LIFO (Last In, First Out) data structure. It's used in multiple frontend scenarios like parsing expressions or evaluating the validity of bracket sequences.

### 7. **WebSockets**:
Provides full-duplex communication channels over a single TCP connection. Useful for live interactions with the server without the overhead of HTTP requests.

```javascript
// Creating a WebSocket connection
const socket = new WebSocket('ws://example.com/socketserver');

socket.onopen = (event) => {
  socket.send('Hello Server!');
};

socket.onmessage = (event) => {
  console.log(`Data received from server: ${event.data}`);
};
```
This code initializes a WebSocket connection to a server. The `onopen` event fires when the connection is established, and `onmessage` is triggered when the client receives data from the server.



### 8. **jQuery**:
A fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, and animation much simpler.

### 9. **Web Workers**:
They run JavaScript code concurrently with the main execution thread. The method `postMessage` is used to send data to the worker.

```javascript
// Main.js
const worker = new Worker('worker.js');

worker.postMessage('Hello, worker!');

worker.onmessage = (event) => {
  console.log(`Received: ${event.data}`);
};

// worker.js
self.onmessage = (event) => {
  console.log(`Worker received: ${event.data}`);
  postMessage('Thanks, main!');
};
```
This demonstrates how web workers operate. In `Main.js`, we create a new web worker and send it a message. The worker (`worker.js`) listens for this message, logs it, and sends a message back.



### 10. **Error Handling**:
Always check for `null` or `undefined` before using an object. It prevents runtime errors and enhances the robustness of the code.

### 11. **HTML5**:
Introduced new semantic elements like `<article>`, `<aside>`, `<details>`, `<figcaption>`, `<figure>`, `<footer>`, `<header>`, and `<hgroup>`. These provide better structure and clarity to web content.


### 12. **Performance**:

Performance in the frontend world is all about making your application feel fast and responsive. It's essential to ensure that JavaScript, which runs in a single-threaded environment (the main thread), doesn't block the rendering of the page, leading to a sluggish user experience.

The JavaScript runtime uses something called the Event Loop, which checks the message queue for pending messages (or tasks) and executes them in the order they were added.

`setInterval` is a method that allows you to run a function repeatedly, starting after the interval of time you specify. This can be useful for tasks like polling a server for updates or updating the UI at fixed intervals.

However, caution is needed. If the function you provide to `setInterval` is computationally heavy or if too many intervals are set, you risk overcrowding the event loop. This can make the page unresponsive.

Let's look at an example:

```javascript
// This will log "Updating..." to the console every 2 seconds
const intervalID = setInterval(() => {
    console.log("Updating...");
}, 2000);

// To stop the above interval, you'd call:
// clearInterval(intervalID);
```

While `setInterval` is useful, there are other performance-enhancing methods and APIs available:

- `requestAnimationFrame`: This is a better option for animations. It tells the browser that you wish to perform an animation and requests that the browser schedules a repaint of the window.
- Web Workers: As mentioned earlier, web workers run JavaScript code concurrently with the main execution thread. This means you can perform heavy computations without blocking the UI.
- Debounce and Throttle: These are techniques to limit the number of times a particularly expensive function runs. This can be beneficial for scroll or resize event handlers.

In summary, while tools like `setInterval` can be beneficial, always be aware of the performance implications of your code. It's crucial to regularly profile and test your applications, especially as they grow and become more complex.


---

**Closing Thoughts**:

Frontend web development is vast and continually evolving. This guide gives a snapshot of some essential topics. Dive deeper into each to gain a solid understanding and keep practicing. Happy coding!

---
