# npmdoc-extend

#### basic api documentation for  [extend (v3.0.0)](https://github.com/justmoon/node-extend#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-extend.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-extend) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-extend.svg)](https://travis-ci.org/npmdoc/node-npmdoc-extend)

#### Port of jQuery.extend for node.js and the browser

[![NPM](https://nodei.co/npm/extend.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/extend)

- [https://npmdoc.github.io/node-npmdoc-extend/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-extend/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-extend/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-extend/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-extend/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-extend/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Stefan Thomas",
        "url": "http://www.justmoon.net"
    },
    "bugs": {
        "url": "https://github.com/justmoon/node-extend/issues"
    },
    "contributors": [
        {
            "name": "Jordan Harband",
            "url": "https://github.com/ljharb"
        }
    ],
    "dependencies": {},
    "description": "Port of jQuery.extend for node.js and the browser",
    "devDependencies": {
        "covert": "^1.1.0",
        "eslint": "^0.24.0",
        "jscs": "^1.13.1",
        "tape": "^4.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "5a474353b9f3353ddd8176dfd37b91c83a46f1d4",
        "tarball": "https://registry.npmjs.org/extend/-/extend-3.0.0.tgz"
    },
    "gitHead": "148e7270cab2e9413af2cd0cab147070d755ed6d",
    "homepage": "https://github.com/justmoon/node-extend#readme",
    "keywords": [
        "extend",
        "clone",
        "merge"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "justmoon"
        },
        {
            "name": "ljharb"
        }
    ],
    "name": "extend",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/justmoon/node-extend.git"
    },
    "scripts": {
        "coverage": "covert test/index.js",
        "coverage-quiet": "covert test/index.js --quiet",
        "eslint": "eslint *.js */*.js",
        "jscs": "jscs *.js */*.js",
        "lint": "npm run jscs && npm run eslint",
        "test": "npm run lint && node test/index.js && npm run coverage-quiet"
    },
    "version": "3.0.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
