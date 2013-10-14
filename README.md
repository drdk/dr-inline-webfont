dr-webfont-inliner
==================

Inline webfonts in stylesheets.


## Command line usage:

```
phantomjs index.js <file> [options]
```

#### Options:

* `-o, --output [string]` - Path to write output to. Defaults to appending `-inline` to input name, eg `style.css` will result in `style-inline.css`.

##### Examples:

Output stylesheet with inlined fonts at the same location as the source:
```
phantomjs index.js style.css
```

Output stylesheet with inlined fonts in another location:
```
phantomjs index.js my/path/style.css -o my/other/path/style.css
```

## Module usage:

### Arguments

* `input` - Path to the stylesheet that needs to get webfonts inlined.
* `output` - Optional. Path to write output to. Defaults to appending `-inline` to input name.

Output stylesheet with inlined fonts at the same location as the source:

```javascript
var inline = require("dr-webfont-inliner");

inline("style.css");
```

Output stylesheet with inlined fonts in another location:

```javascript
var inline = require("dr-webfont-inliner");

inline("my/path/style.css", "my/other/path/style.css")
```
