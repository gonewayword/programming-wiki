[<< back to table of contents](https://github.com/hackreactor/2016-04-peripheral-brain/wiki)

## What is the DOM?
* Stands for Document Object Model
* W3C (World Wide Web Consortium) standard for browsers, defined as "a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document."
* The HTML DOM is structured as a tree of object/elements

## How would you design the DOM, if you had to make it from scratch?
* slnjf
* dsifnkjd

## Outline how browsers keep your data secure
* The most common type of browser data attack is XSS, or Cross Site Scripting
	* XSS enables attackers to inject client-side scripts into web pages viewed by other users
* The basic protection for browser user data is the same-origin policy
* With same-origin, a web browser permits scripts contained in a first web page to access data in a second web page, but only if both web pages have the same origin.
* An origin is defined as a combination of URI scheme, hostname, and port number
* Cross-site scripting can often bypass same-origin policy, so other protections are needed

### Basic Defense Against XSS
* The most basic defense against XSS is contextual encoding/escaping of string input
...This is a way of sanitizing URIs or string inputs to ensure they do not contain anything modifying client-side scripts
* Validating untrusted HTML input with HTML Sanitization engines
* Cookie Security - many sites tie the session's cookie/s to one particular IP address and do not allow access to that cookied session by anyone but that IP address
* Disabling Client Side Scripts - This is blocking client-side sripts entirely, until a user knows that the website is trustworth and problem-free, and can then allow client-side scripts to operate. Some browsers have this functionality built in, and some products like [NoScript](https://en.wikipedia.org/wiki/NoScript) offer an advanced version.

### Newest, evolving methods of preventing XSS

*  [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy), Javascript sandbox tools, and auto-escaping templates are all emerging methods to combat XSS

## What is a virtual DOM?

* A virtual DOM is a lightweight, 'copy' version of the DOM.
* Created because the DOM itself can be extremely slow, for example, if attempting to move one thousand DIVs one inch to the left
* The virtual DOM can be operated on much more rapidly, and with the minimal required interaction with the real DOM
* The most famous example may be React JS, which creates a lightweight tree mimicking the DOM (a virtual DOM), generates HTML based on the code, and appends it to the real DOM

## What happens when you load a page?
### Async vs. Defer

* The moment a web page loads, the browser begins parsing the HTML file
* The moment the browser hits a script file, parsing is paused and it will load that script file, and resume parsing as necessary
* __Async Script Tag__: An async script tag, as such, `<script async>`, downloads the file during HTML parsing and will pause the HTML parser to execute it when it has finished downloading.
* __Defer Script Tag__: A `<script defer>` script tag downloads the script file during HTML parsing and will only execute it after the parser has completed. Defer scripts are also guaranteed to execute in the order that they appear in the document.

### Pagination and eager loading

#### Three types of loading

* Eager loading: Load all pages at once before you render them to the user
* Lazy loading: Load pages or images/assets only as needed (i.e. as visited by user)
* Over-eager loading: Loading pages/assets in anticipation of their future need by a user--attempting to anticipate what a user will want and having those assets already loaded

## Event handling and bubbling
### Event delegation
* Event delegation is the delegating of responsibility for a click event to other DOM elements than the element actually containing said Event
* For example, the following list:
```
<ul onclick="alert(event.type + '!')">
    <li>One</li>
    <li>Two</li>
    <li>Three</li>
	 </ul>
```
* The child elements, when clicked, will trigger the parent's click event.
* Event bubbling specifically refers to bubbling event handlers from the source child, all the way up to even the document levelgit
