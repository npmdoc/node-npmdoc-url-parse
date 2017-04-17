# api documentation for  [url-parse (v1.1.8)](https://github.com/unshiftio/url-parse#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-url-parse.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-url-parse) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-url-parse.svg)](https://travis-ci.org/npmdoc/node-npmdoc-url-parse)
#### Small footprint URL parser that works seamlessly across Node.js and browser environments

[![NPM](https://nodei.co/npm/url-parse.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/url-parse)

- [https://npmdoc.github.io/node-npmdoc-url-parse/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-url-parse/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-url-parse/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-url-parse/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-url-parse/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-url-parse/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Arnout Kazemier"
    },
    "bugs": {
        "url": "https://github.com/unshiftio/url-parse/issues"
    },
    "dependencies": {
        "querystringify": "0.0.x",
        "requires-port": "1.0.x"
    },
    "description": "Small footprint URL parser that works seamlessly across Node.js and browser environments",
    "devDependencies": {
        "assume": "1.4.x",
        "browserify": "~14.1.0",
        "istanbul": "0.4.x",
        "mocha": "~3.2.0",
        "pre-commit": "~1.2.0",
        "zuul": "3.11.x"
    },
    "directories": {},
    "dist": {
        "shasum": "7a65b3a8d57a1e86af6b4e2276e34774167c0156",
        "tarball": "https://registry.npmjs.org/url-parse/-/url-parse-1.1.8.tgz"
    },
    "gitHead": "daacb5a98f64e69ba9cfb01bb7afbde68b756c12",
    "homepage": "https://github.com/unshiftio/url-parse#readme",
    "keywords": [
        "URL",
        "parser",
        "uri",
        "url",
        "parse",
        "query",
        "string",
        "querystring",
        "stringify"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "3rdeden"
        },
        {
            "name": "swaagie"
        },
        {
            "name": "unshift"
        },
        {
            "name": "v1"
        }
    ],
    "name": "url-parse",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/unshiftio/url-parse.git"
    },
    "scripts": {
        "100%": "istanbul check-coverage --statements 100 --functions 100 --lines 100 --branches 100",
        "browserify": "mkdir -p dist && browserify index.js -s URLParse -o dist/url-parse.js",
        "coverage": "istanbul cover _mocha -- test.js",
        "test": "mocha test.js",
        "test-browser": "zuul -- test.js",
        "test-node": "istanbul cover _mocha --report lcovonly -- test.js",
        "watch": "mocha --watch test.js"
    },
    "version": "1.1.8"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
