# Breakpoint
Breakpoint responds to screen size and applies viewport breakpoint classes to the document element. It has no dependencies.

Minified version is 917 bytes.

__Status: Working, just mulling over the class names__

# Usage

Include breakpoint.min.js in your web app in the normal way:

```
<script src="breakpoint.min.js"></script>
```

Breakpoint has no dependencies and can be used standalone and should not interfere with any JavaScript libraries or frameworks.

# Rough Illustration

If the breakpoints array = [768] then

```
At Screen Width     Classes on the HTML Element
-----------------------------------------------
320                 lte768
768                 lte768
1024                gt768
```

If the breakpoints array = [768, 320] then

```
At Screen Width     Classes on the HTML Element
-----------------------------------------------
320                 lte320 lte768
768                 gt320 gt320lte768 lte768
1024                gt320 gt768
```

# Test Page
See http://www.dave-smith.info/breakpoint/tests/test1.html or download breakpoint and try out the test page where breakpoints can be edited on the fly.

# Using Custom Breakpoints

Push new ones onto the default array:

```
window['https://github.com/davesmith/breakpoint'].push(456);
```

Or use a completely new set of breakpoints, which overwrites the default:

```
window['https://github.com/davesmith/breakpoint'].breakpoints = [320, 768];
```

# Perform a Manual Update
The update function is called when the window resizes. If the breakpoints array
is modified dynamically then an update can be called without needing to resize the window.

```
window['https://github.com/davesmith/breakpoint'].update();
```