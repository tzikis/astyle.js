astyle.js
=========

The well-known [Artistic Style](http://astyle.sourceforge.net/) code beautifier, "compiled" to JavaScript.

Usage
=========

Include the javacsript file:

```html
<script src="path/to/astyle.js"></script>
```

Define a js function to call the c function:

```javascript
js_format_string = Module.cwrap('js_format_string', 'string', ['string']);
```

call the function:

```javascript
formatted_string = js_format_string("#include<stdio.h>\n int main(void) {\n           sleep(0);\nsleep(0);\n\t\tsleep(0);\n }");
```

output:
```javascript
console.log(formatted_string);
```

```
#include<stdio.h>
int main(void)
{
	sleep(0);
	sleep(0);
	sleep(0);
} 
```

Note that, right now, it's hardcoded to use hard tabs, and one indentation style (you know, the right one! :P).
