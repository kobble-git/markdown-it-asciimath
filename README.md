# markdown-it-asciimath
Markdown-it plugin to include ascii-math. Still under Development.

**Code block**

Example input:
```md
    ```math
    1+1=2
    varphi = int_0^10 x^2 dx
    ```
```

Output: HTML, renders to:

![math output](https://cloud.githubusercontent.com/assets/18582541/18347144/3c7e5aaa-75c4-11e6-888f-c8e6f406fdc7.png)

**Inline math**

Example input:
```md
    Test `math 1+1=2` test.
```

## Usage
markdown-it-asciimath converts ASCII-math to TeX and then uses KaTeX to render the math. The ASCII-math - TeX conversion is done using the [ASCIIMathML](https://github.com/mathjax/asciimathml) Scripts. The following file needs to be included:

```html
<script src="./node_modules/markdown-it-asciimath/ASCIIMathTeXImg.js"></script>
```

The plugin uses KaTeX to render TeX-math so the KaTeX stylesheet needs to be included:

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.6.0/katex.min.css">
```

To use the plugin:

```javascript
var md = require('markdown-it')();

md.use(require("./node_modules/markdown-it-asciimath/index.js"));
```
