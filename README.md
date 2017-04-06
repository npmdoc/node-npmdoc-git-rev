# api documentation for  [git-rev (v0.2.1)](https://github.com/tblobaum/git-rev)  [![npm package](https://img.shields.io/npm/v/npmdoc-git-rev.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-git-rev) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-git-rev.svg)](https://travis-ci.org/npmdoc/node-npmdoc-git-rev)
#### get the current git commit hash, tag or branch in node

[![NPM](https://nodei.co/npm/git-rev.png?downloads=true)](https://www.npmjs.com/package/git-rev)

[![apidoc](https://npmdoc.github.io/node-npmdoc-git-rev/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-git-rev_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-git-rev/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-git-rev/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-git-rev/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Thomas Blobaum",
        "email": "tblobaum@gmail.com",
        "url": "https://github.com/tblobaum/"
    },
    "bin": {},
    "bugs": {
        "url": "https://github.com/tblobaum/git-rev/issues"
    },
    "dependencies": {},
    "description": "get the current git commit hash, tag or branch in node",
    "devDependencies": {},
    "directories": {
        "example": "example"
    },
    "dist": {
        "shasum": "8ccbd2092b345bc2c9149548396df549646ca63f",
        "tarball": "https://registry.npmjs.org/git-rev/-/git-rev-0.2.1.tgz"
    },
    "homepage": "https://github.com/tblobaum/git-rev",
    "keywords": [],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "tblobaum",
            "email": "tblobaum@gmail.com"
        }
    ],
    "name": "git-rev",
    "optionalDependencies": {},
    "readme": "# git-rev\n\naccess git revision state in node\n\n# Example\n\n''' js\nvar git = require('git-rev')\n\ngit.short(function (str) {\n  console.log('short', str)\n  // => aefdd94\n})\n\ngit.long(function (str) {\n  console.log('long', str)\n  // => aefdd946ea65c88f8aa003e46474d57ed5b291d1\n})\n\ngit.branch(function (str) {\n  console.log('branch', str)\n  // => master\n})\n\ngit.tag(function (str) {\n  console.log('tag', str)\n  // => 0.1.0\n})\n\n'''\n\n# Methods\n\n''' js \nvar git = require('git-rev')\n'''\n\n## .log(function (array) { ... })\nreturn the git log of 'process.cwd()' as an array\n\n''' js\ngit.log(function (array) {\n  console.log('log', array)\n  // [ [ 'aefdd946ea65c88f8aa003e46474d57ed5b291d1',\n  //     'add description',\n  //     '7 hours ago',\n  //     'Thomas Blobaum' ],\n  //   [ '1eb9a6c8633a5a47a47487f17b17ae545d0e26a8',\n  //     'first',\n  //     '7 hours ago',\n  //     'Thomas Blobaum' ],\n  //   [ '7f85b750b908d28bfeb13ad6dba47d9d604508f9',\n  //     'first commit',\n  //     '2 days ago',\n  //     'Thomas Blobaum' ] ]\n})\n'''\n\n## .short(function (commit) { ... })\nreturn the result of 'git rev-parse --short HEAD'\n\n## .long(function (commit) { ... })\nreturn the result of 'git rev-parse HEAD'\n\n## .tag(function (tag) { ... })\nreturn the current tag\n\n## .branch(function (branch) { ... })\nreturn the current branch\n\n# Install\n\n'npm install git-rev'\n\n# License\n\n(The MIT License)\n\nCopyright (c) 2012 Thomas Blobaum <tblobaum@gmail.com>\n\nPermission is hereby granted, free of charge, to any person obtaining\na copy of this software and associated documentation files (the\n'Software'), to deal in the Software without restriction, including\nwithout limitation the rights to use, copy, modify, merge, publish,\ndistribute, sublicense, and/or sell copies of the Software, and to\npermit persons to whom the Software is furnished to do so, subject to\nthe following conditions:\n\nThe above copyright notice and this permission notice shall be\nincluded in all copies or substantial portions of the Software.\n\nTHE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,\nEXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF\nMERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.\nIN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY\nCLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,\nTORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE\nSOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.\n",
    "readmeFilename": "README.md",
    "repository": {
        "type": "git",
        "url": "git://github.com/tblobaum/git-rev.git"
    },
    "scripts": {},
    "version": "0.2.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module git-rev](#apidoc.module.git-rev)
1.  [function <span class="apidocSignatureSpan">git-rev.</span>branch (cb)](#apidoc.element.git-rev.branch)
1.  [function <span class="apidocSignatureSpan">git-rev.</span>log (cb)](#apidoc.element.git-rev.log)
1.  [function <span class="apidocSignatureSpan">git-rev.</span>long (cb)](#apidoc.element.git-rev.long)
1.  [function <span class="apidocSignatureSpan">git-rev.</span>short (cb)](#apidoc.element.git-rev.short)
1.  [function <span class="apidocSignatureSpan">git-rev.</span>tag (cb)](#apidoc.element.git-rev.tag)



# <a name="apidoc.module.git-rev"></a>[module git-rev](#apidoc.module.git-rev)

#### <a name="apidoc.element.git-rev.branch"></a>[function <span class="apidocSignatureSpan">git-rev.</span>branch (cb)](#apidoc.element.git-rev.branch)
- description and source-code
```javascript
branch = function (cb) {
  _command('git rev-parse --abbrev-ref HEAD', cb)
}
```
- example usage
```shell
...
})

git.long(function (str) {
console.log('long', str)
// => aefdd946ea65c88f8aa003e46474d57ed5b291d1
})

git.branch(function (str) {
console.log('branch', str)
// => master
})

git.tag(function (str) {
console.log('tag', str)
// => 0.1.0
...
```

#### <a name="apidoc.element.git-rev.log"></a>[function <span class="apidocSignatureSpan">git-rev.</span>log (cb)](#apidoc.element.git-rev.log)
- description and source-code
```javascript
log = function (cb) {
  _command('git log --no-color --pretty=format:\'[ "%H", "%s", "%cr", "%an" ],\' --abbrev-commit', function (str) {
    str = str.substr(0, str.length-1)
    cb(JSON.parse('[' + str + ']'))
  })
}
```
- example usage
```shell
...

# Example

''' js
var git = require('git-rev')

git.short(function (str) {
  console.log('short', str)
  // => aefdd94
})

git.long(function (str) {
  console.log('long', str)
  // => aefdd946ea65c88f8aa003e46474d57ed5b291d1
})
...
```

#### <a name="apidoc.element.git-rev.long"></a>[function <span class="apidocSignatureSpan">git-rev.</span>long (cb)](#apidoc.element.git-rev.long)
- description and source-code
```javascript
long = function (cb) {
  _command('git rev-parse HEAD', cb)
}
```
- example usage
```shell
...
var git = require('git-rev')

git.short(function (str) {
console.log('short', str)
// => aefdd94
})

git.long(function (str) {
console.log('long', str)
// => aefdd946ea65c88f8aa003e46474d57ed5b291d1
})

git.branch(function (str) {
console.log('branch', str)
// => master
...
```

#### <a name="apidoc.element.git-rev.short"></a>[function <span class="apidocSignatureSpan">git-rev.</span>short (cb)](#apidoc.element.git-rev.short)
- description and source-code
```javascript
short = function (cb) {
  _command('git rev-parse --short HEAD', cb)
}
```
- example usage
```shell
...
access git revision state in node

# Example

''' js
var git = require('git-rev')

git.short(function (str) {
console.log('short', str)
// => aefdd94
})

git.long(function (str) {
console.log('long', str)
// => aefdd946ea65c88f8aa003e46474d57ed5b291d1
...
```

#### <a name="apidoc.element.git-rev.tag"></a>[function <span class="apidocSignatureSpan">git-rev.</span>tag (cb)](#apidoc.element.git-rev.tag)
- description and source-code
```javascript
tag = function (cb) {
  _command('git describe --always --tag --abbrev=0', cb)
}
```
- example usage
```shell
...
})

git.branch(function (str) {
  console.log('branch', str)
  // => master
})

git.tag(function (str) {
  console.log('tag', str)
  // => 0.1.0
})

'''

# Methods
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
