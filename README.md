# api documentation for  [url-parse (v1.1.8)](https://github.com/unshiftio/url-parse#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-url-parse.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-url-parse) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-url-parse.svg)](https://travis-ci.org/npmdoc/node-npmdoc-url-parse)
#### Small footprint URL parser that works seamlessly across Node.js and browser environments

[![NPM](https://nodei.co/npm/url-parse.png?downloads=true)](https://www.npmjs.com/package/url-parse)

[![apidoc](https://npmdoc.github.io/node-npmdoc-url-parse/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-url-parse_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-url-parse/build/apidoc.html)

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
            "name": "3rdeden",
            "email": "npm@3rd-Eden.com"
        },
        {
            "name": "swaagie",
            "email": "info@martijnswaagman.nl"
        },
        {
            "name": "unshift",
            "email": "npm@unshift.io"
        },
        {
            "name": "v1",
            "email": "npm@3rd-Eden.com"
        }
    ],
    "name": "url-parse",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module url-parse](#apidoc.module.url-parse)
1.  [function <span class="apidocSignatureSpan">url-parse.</span>extractProtocol (address)](#apidoc.element.url-parse.extractProtocol)
1.  [function <span class="apidocSignatureSpan">url-parse.</span>location (loc)](#apidoc.element.url-parse.location)
1.  object <span class="apidocSignatureSpan">url-parse.</span>qs

#### [module url-parse.qs](#apidoc.module.url-parse.qs)
1.  [function <span class="apidocSignatureSpan">url-parse.qs.</span>parse (query)](#apidoc.element.url-parse.qs.parse)
1.  [function <span class="apidocSignatureSpan">url-parse.qs.</span>stringify (obj, prefix)](#apidoc.element.url-parse.qs.stringify)



# <a name="apidoc.module.url-parse"></a>[module url-parse](#apidoc.module.url-parse)

#### <a name="apidoc.element.url-parse.extractProtocol"></a>[function <span class="apidocSignatureSpan">url-parse.</span>extractProtocol (address)](#apidoc.element.url-parse.extractProtocol)
- description and source-code
```javascript
function extractProtocol(address) {
  var match = protocolre.exec(address);

  return {
    protocol: match[1] ? match[1].toLowerCase() : '',
    slashes: !!match[2],
    rest: match[3]
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-parse.location"></a>[function <span class="apidocSignatureSpan">url-parse.</span>location (loc)](#apidoc.element.url-parse.location)
- description and source-code
```javascript
function lolcation(loc) {
  loc = loc || global.location || {};
  URL = URL || require('./');

  var finaldestination = {}
    , type = typeof loc
    , key;

  if ('blob:' === loc.protocol) {
    finaldestination = new URL(unescape(loc.pathname), {});
  } else if ('string' === type) {
    finaldestination = new URL(loc, {});
    for (key in ignore) delete finaldestination[key];
  } else if ('object' === type) {
    for (key in loc) {
      if (key in ignore) continue;
      finaldestination[key] = loc[key];
    }

    if (finaldestination.slashes === undefined) {
      finaldestination.slashes = slashes.test(loc.href);
    }
  }

  return finaldestination;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.url-parse.qs"></a>[module url-parse.qs](#apidoc.module.url-parse.qs)

#### <a name="apidoc.element.url-parse.qs.parse"></a>[function <span class="apidocSignatureSpan">url-parse.qs.</span>parse (query)](#apidoc.element.url-parse.qs.parse)
- description and source-code
```javascript
function querystring(query) {
  var parser = /([^=?&]+)=?([^&]*)/g
    , result = {}
    , part;

  //
  // Little nifty parsing hack, leverage the fact that RegExp.exec increments
  // the lastIndex property so we can continue executing this loop until we've
  // parsed all results.
  //
  for (;
    part = parser.exec(query);
    result[decodeURIComponent(part[1])] = decodeURIComponent(part[2])
  );

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.url-parse.qs.stringify"></a>[function <span class="apidocSignatureSpan">url-parse.qs.</span>stringify (obj, prefix)](#apidoc.element.url-parse.qs.stringify)
- description and source-code
```javascript
function querystringify(obj, prefix) {
  prefix = prefix || '';

  var pairs = [];

  //
  // Optionally prefix with a '?' if needed
  //
  if ('string' !== typeof prefix) prefix = '?';

  for (var key in obj) {
    if (has.call(obj, key)) {
      pairs.push(encodeURIComponent(key) +'='+ encodeURIComponent(obj[key]));
    }
  }

  return pairs.length ? prefix + pairs.join('&') : '';
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
