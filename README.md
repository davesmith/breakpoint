# Breakpoint
Breakpoint responds to screen size and applies viewport breakpoint classes to the document element

Minified version is 907 bytes.

__Status: Working, mulling over the class names__

# Test Page
Download breakpoint and try out the test page where breakpoints can be edited on the fly.

# Quick Illustration
```

// If the breakpoint array = [768]

At Screen Width  Classes on the HTML Element
320              lte768
768              lte768
1024             gt768


// If the breakpoint array = [768, 320]

At Screen Width  Classes on the HTML Element
320              lte320 lte768 lte320lte768
768              gt320  lte768 gt320lte768
800              gt320  gt768  gt320gt768

```

# In the pipeline
1. Avoid outputting non-sense classes like lte320lte768