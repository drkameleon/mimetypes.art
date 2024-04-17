<h1 align="center">
    Mimetypes
</h1>

<p align="center">
     <i>Mimetype recognition package for  Arturo</i> 
     <br><br>
     <img src="https://img.shields.io/github/license/arturo-lang/grafito?style=for-the-badge">
    <img src="https://img.shields.io/badge/language-Arturo-orange.svg?style=for-the-badge">
</p>

--- 
 
<!--ts-->

* [What does this package do?](#what-does-this-package-do)
* [How do I use it?](#how-do-i-use-it)
* [Function Reference](#function-reference)
* [License](#license)   

<!--te-->
 
---

### What does this package do?

This package provides an ample (2000+) entry database of MIME content typse and their corresponding extensions and allows to easily look up the suitable extensions by file extension (or file path). It also supports the reverse operation: look up possible mime types, based on a given extension.

> [!TIP]
> For the data, the package has been based on the very useful list compiled by the [mime-db](https://github.com/jshttp/mime-db) project.

### How do I use it?

Simply `import` it and use the included `mimetype` function:

```arturo
import "mimetypes"!

mimetype "jpg"              ; => ["image/jpeg"]
mimetype "somefile.jpg"     ; => ["image/jpeg"]
mimetype "boom"             ; => []

mimetype.extensions "image/jpeg"
; => ["jpe","jpeg","jpg"]
```

> [!IMPORTANT]
> In case no suitable MIME type has been found for a given extension/path, or if the given MIME type isn't associated with any known extensions, then `mimetype` will return an empty block!

### Function reference

#### `mimetype`

##### Description

get mimetype(s) from given extension/filepath

##### Usage

<pre>
<b>mimetype</b> <ins>location</ins> <i>:string</i>
</pre>

##### Attributes

| Option | Type(s) | Description |
|----|----|----|
| extensions |  | get possible file extensions for given mimetype instead | 

##### Returns

- *:block*

<hr/>

### License

MIT License

Copyright (c) 2024 Yanis Zafirópulos

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
