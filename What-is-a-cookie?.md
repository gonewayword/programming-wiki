[<< back to table of contents](https://github.com/hackreactor/2016-04-peripheral-brain/wiki)

## What is the DOM?

## How would you design the DOM, if you had to make it from scratch?
## Outline how browsers keep your data secure
## What is a virtual DOM?
## What happens when you load a page?
	## Async vs. Defer
	## Pagination and eager loading
## Event handling and bubbling
	## Event delegation

## Background

* defined in an RFC(todo) [in 1997](https://tools.ietf.org/html/rfc2109), as an extension of the HTTP protocol(todo)
* "Cookie" [[HTTP]] header
* key-value pairs
* sent with every HTTP request
* the primary way to get around HTTP's stateless nature
* scoped by subdomain
* can be set to expire

## How is it used?
* remembering stateful information, e.g. items in a shopping cart or previously entered items in a form field
* implementing sessions. For example, an encrypted session id can be stored in the cookie.
* generally, storing any client-specific data
* user tracking across sites

## Tips/Gotchas
* They only store up to around 4KB
* you can encrypt them but it's safer to just use them to store an id, keyed to fetch the full user info, server-side
* you can relax the scoping to just the domain to share cookies between subdomains, this is one way to get a poor man's SSO(todo)
* setting them to never expire is often a security risk
* since they're sent with every request, they can waste bandwidth
* can fix this by putting static assets on a separate subdomain or domain

## See also
* HTTP protocol
* stateless design
* same-origin policy
* sessions
* single-sign-on
