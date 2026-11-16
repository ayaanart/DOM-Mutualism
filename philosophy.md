# Philosophy
Value is our core identity and our beliefs.
The principles are how we are implementing our values in big picture; they do not go into how the exact specific implementation works.
Together I believe they make a philosophy.
I am not going to say which principles correlate to which values as it is not 1:1,
and they also contribute to different values to different degrees;
thinking for a few seconds will probably give you a clearer idea.

## Values
- Technical: These pages are designed for more technical users (as in the end-user viewing the page) compared to the average web users
- Predictability: Pages that work in predictable ways
- Delegation: Each language should do what it is good at; we should capitalize on things languages provide for free
- Transparent: Users of the lib should know what the lib is doing. The lib should facilitate, not abstractize
- Styling: CSS components are designed to be easily customized or overwritten by page viewers.
- Debugging: Errors of the page are made obvious and clear to both developers and users of the page who use the console
- Open: These pages are meant to run only in your browser and be open-source.
I would **not** use it for sites that need security.
Think local game instead of a web page with many users interacting and logins.

## Principles

### Mutualism
Provides tools to help HTML, CSS, and JS work together, but separately.
Each of those languages does what it was designed to do.
No language oversteps into another territory
- JS: logic, drawing on the canvas, state manager
- CSS: presenting, responding to state changes
- HTML: Underlying structure of the page, buttons, text, UI

JS changes classes or data-attributes, and CSS reacts to them.

### Readable
Can be practically read by a serious user.
The variable names are clear and each function has its own JSDoc.
The code is modular and aims to keep individual files <500 lines,
but this is not a strict limit, and content matters far more.
The general rule is if they do not share the need to access the same internal state and they are distinct concepts then split into separate modules.

### Non-abstract
It is designed to be a formalization and/or facilitation rather than an abstraction.
The lib doesn’t hide the DOM or canvas from you;
it wraps patterns in a clear, named form.
This means functions refer to what is actually happening, and not an abstract layer.
A new web developer using this lib would learn more about the browser rather than this framework.

### Browser-focused
Specially designed to make browser applications.
Whether the code can run outside a browser is not in the scope.

### No-dependencies
You can easily and smoothly use this lib without downloading extra software, such as Node.js.
This can be the only lib you use for a browser application.
- It provides helpers allowing you not to install other libs for utility.
- It expects the console for debugging keeping you in the browser.

### Loud fails
Clear and early errors that say which function failed and what args they received.
It does not rely on JS automatic error messages.

### Override
The CSS Variables (Custom Properties) is designed in a way that is meant to be overwritten/customized.
For example: text size, fonts, and colors.
We will focus on:
- Clear patterns
- Not locked down CSS
- Safety checks/capping so your layout does not completely break in unexpected ways that the user setting the override could not predict.
E.g. setting text size to big.
