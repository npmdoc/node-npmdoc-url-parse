# npmdoc-url-parse

#### api documentation for  url-parse (v1.1.8)  [![npm package](https://img.shields.io/npm/v/npmdoc-url-parse.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-url-parse) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-url-parse.svg)](https://travis-ci.org/npmdoc/node-npmdoc-url-parse)

#### Small footprint URL parser that works seamlessly across Node.js and browser environments

[![NPM](https://nodei.co/npm/url-parse.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/url-parse)

- [https://npmdoc.github.io/node-npmdoc-url-parse/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-url-parse/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-url-parse/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-url-parse/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-url-parse/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-url-parse/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "url-parse",
    "version": "1.1.8",
    "description": "Small footprint URL parser that works seamlessly across Node.js and browser environments",
    "main": "index.js",
    "scripts": {
        "100%": "istanbul check-coverage --statements 100 --functions 100 --lines 100 --branches 100",
        "browserify": "mkdir -p dist && browserify index.js -s URLParse -o dist/url-parse.js",
        "test-node": "istanbul cover _mocha --report lcovonly -- test.js",
        "coverage": "istanbul cover _mocha -- test.js",
        "test-browser": "zuul -- test.js",
        "watch": "mocha --watch test.js",
        "test": "mocha test.js"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/unshiftio/url-parse.git"
    },
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
    "author": "Arnout Kazemier",
    "license": "MIT",
    "dependencies": {
        "querystringify": "0.0.x",
        "requires-port": "1.0.x"
    },
    "devDependencies": {
        "assume": "1.4.x",
        "browserify": "~14.1.0",
        "istanbul": "0.4.x",
        "mocha": "~3.2.0",
        "pre-commit": "~1.2.0",
        "zuul": "3.11.x"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
