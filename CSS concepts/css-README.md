Table of contents

1. [ before and after pseudo element](#before-and-after-pseudo-element)


## before-and-after-pseudo-element
::before and ::after are two invisible elements that CSS can create inside an element.

eg:
```
h1::before {
    content: "👉 ";
}

h1::after {
    content: " 👈";
}

result:
👉 Hello 👈
```
How the browser treats is:
[before] Hello [after]

Note: Content property is required to place the elements.
