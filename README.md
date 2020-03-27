# gulp-src-combine [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][depstat-image]][depstat-url]

## Usage

First, install `gulp-src-combine` as a development dependency:

```shell
npm install --save-dev gulp-src-combine
```

```javascript
var gsc = require("gulp-src-combine");

gulp.src('./sample.js')
  .pipe(gsc({
    "/* file 1 */": "tmp/file1",
    "/* file 2 */": "tmp/file2",
    version: "tmp/version_number"
  }))
  .pipe(gulp.dest('./dist/'));
```
This will replace into sample.js the tag "/\* file 1 \*/" by the content of the file "tmp/file1", "/\* file 2 \*/" by the content of "tmp/file2" and "version" by the content of "tmp/version_number" each time they appear.

Based on `gulp-file-insert` but has been updated.

## LICENSE

(MIT License)

Copyright (c) 2018 warloque <solidkey@gmail.com>
Copyright (c) 2014 Jean-Baptiste DEMONTE <jbdemonte@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


[npm-url]: https://npmjs.org/package/gulp-src-combine
[npm-image]: https://badge.fury.io/js/gulp-src-combine.png

[travis-url]: http://travis-ci.org/warloque/gulp-src-combine
[travis-image]: https://travis-ci.org/warloque/gulp-src-combine.svg?branch=master

[depstat-url]: https://david-dm.org/warloque/gulp-src-combine
[depstat-image]: https://david-dm.org/warloque/gulp-src-combine.png