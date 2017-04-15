# api documentation for  [extend (v3.0.0)](https://github.com/justmoon/node-extend#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-extend.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-extend) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-extend.svg)](https://travis-ci.org/npmdoc/node-npmdoc-extend)
#### Port of jQuery.extend for node.js and the browser

[![NPM](https://nodei.co/npm/extend.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/extend)

[![apidoc](https://npmdoc.github.io/node-npmdoc-extend/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-extend/build/apidoc.html)

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
    "version": "3.0.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module extend](#apidoc.module.extend)
1.  [function <span class="apidocSignatureSpan"></span>extend ()](#apidoc.element.extend.extend)
1.  [function <span class="apidocSignatureSpan">extend.</span>toString ()](#apidoc.element.extend.toString)



# <a name="apidoc.module.extend"></a>[module extend](#apidoc.module.extend)

#### <a name="apidoc.element.extend.extend"></a>[function <span class="apidocSignatureSpan"></span>extend ()](#apidoc.element.extend.extend)
- description and source-code
```javascript
function extend() {
	var options, name, src, copy, copyIsArray, clone,
		target = arguments[0],
		i = 1,
		length = arguments.length,
		deep = false;

	// Handle a deep copy situation
	if (typeof target === 'boolean') {
		deep = target;
		target = arguments[1] || {};
		// skip the boolean and the target
		i = 2;
	} else if ((typeof target !== 'object' && typeof target !== 'function') || target == null) {
		target = {};
	}

	for (; i < length; ++i) {
		options = arguments[i];
		// Only deal with non-null/undefined values
		if (options != null) {
			// Extend the base object
			for (name in options) {
				src = target[name];
				copy = options[name];

				// Prevent never-ending loop
				if (target !== copy) {
					// Recurse if we're merging plain objects or arrays
					if (deep && copy && (isPlainObject(copy) || (copyIsArray = isArray(copy)))) {
						if (copyIsArray) {
							copyIsArray = false;
							clone = src && isArray(src) ? src : [];
						} else {
							clone = src && isPlainObject(src) ? src : {};
						}

						// Never move original objects, clone them
						target[name] = extend(deep, clone, copy);

					// Don't bring in undefined values
					} else if (typeof copy !== 'undefined') {
						target[name] = copy;
					}
				}
			}
		}
	}

	// Return the modified object
	return target;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.extend.toString"></a>[function <span class="apidocSignatureSpan">extend.</span>toString ()](#apidoc.element.extend.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
