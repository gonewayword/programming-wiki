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

## Basic Defense Against XSS
* The most basic defense against XSS is contextual encoding/escaping of string input
	* This is a way of sanitizing URIs or string inputs to ensure they do not contain anything modifying client-side scripts
* Validating untrusted HTML input with HTML Sanitization engines
* Cookie Security - many sites tie the session's cookie/s to one particular IP address and do not allow access to that cookied session by anyone but that IP address
* Disabling Client Side Scripts - This is blocking client-side sripts entirely, until a user knows that the website is trustworth and problem-free, and can then allow client-side scripts to operate. Some browsers have this functionality built in, and some products like [NoScript](https://en.wikipedia.org/wiki/NoScript) offer an advanced version.

## Newest, evolving methods of preventing XSS

*  [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy), Javascript sandbox tools, and auto-escaping templates are all emerging methods to combat XSS

## What is a virtual DOM?



## What happens when you load a page?
	* Async vs. Defer
	* Pagination and eager loading
## Event handling and bubbling
	## Event delegation
