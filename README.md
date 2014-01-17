astyle.js
=========

The well-known [Artistic Style](http://astyle.sourceforge.net/) code beautifier, "compiled" to JavaScript.

Usage
=========

Include the javacsript file:

```
<script src="path/to/astyle.js"></script>
```

Define a js function to call the c function:

```javascript
js_format_string = Module.cwrap('js_format_string', 'string', ['string']);
```

```javascript
formatted_string = js_format_string("#include<stdio.h>\n int main(void) {\n           sleep(0);\nsleep(0);\n\t\tsleep(0);\n }");
```
