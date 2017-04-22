# npmdoc-mochawesome

#### api documentation for  [mochawesome (v2.0.5)](https://github.com/adamgruber/mochawesome#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-mochawesome.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mochawesome) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mochawesome.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mochawesome)

#### A Gorgeous HTML/CSS Reporter for Mocha.js

[![NPM](https://nodei.co/npm/mochawesome.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/mochawesome)

- [https://npmdoc.github.io/node-npmdoc-mochawesome/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-mochawesome/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mochawesome/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mochawesome/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mochawesome/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mochawesome/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Adam Gruber"
    },
    "bugs": {
        "url": "https://github.com/adamgruber/mochawesome/issues"
    },
    "dependencies": {
        "babel-runtime": "^6.20.0",
        "chalk": "^1.1.3",
        "diff": "^3.0.0",
        "fs-extra": "^2.0.0",
        "json-stringify-safe": "^5.0.1",
        "lodash": "^4.17.3",
        "mochawesome-report-generator": "^1.1.0",
        "uuid": "^3.0.1"
    },
    "description": "A Gorgeous HTML/CSS Reporter for Mocha.js",
    "devDependencies": {
        "babel-cli": "^6.18.0",
        "babel-core": "^6.20.0",
        "babel-plugin-istanbul": "^3.0.0",
        "babel-plugin-transform-runtime": "^6.15.0",
        "babel-preset-es2015": "^6.14.0",
        "babel-preset-stage-3": "^6.11.0",
        "babel-register": "^6.14.0",
        "cross-env": "^3.1.2",
        "eslint": "^3.10.2",
        "eslint-config-airbnb-base": "^10.0.1",
        "eslint-plugin-import": "^2.2.0",
        "mocha": "*",
        "nyc": "^9.0.1",
        "proxyquire": "^1.7.10",
        "should": "^11.1.2",
        "sinon": "^1.17.5"
    },
    "directories": {},
    "dist": {
        "shasum": "0ada6c7c27d59ce15ae1ed6736ce84e151f3a0d4",
        "tarball": "https://registry.npmjs.org/mochawesome/-/mochawesome-2.0.5.tgz"
    },
    "engine": "node >= 4",
    "files": [
        "LICENSE.md",
        "README.md",
        "CHANGELOG.md",
        "addContext.js",
        "dist"
    ],
    "gitHead": "28951e0e018682b9af68f37d21745c5c78f2206c",
    "homepage": "https://github.com/adamgruber/mochawesome#readme",
    "keywords": [
        "mocha",
        "reporter",
        "json",
        "html"
    ],
    "license": "MIT",
    "main": "dist/mochawesome.js",
    "maintainers": [
        {
            "name": "adamgruber"
        }
    ],
    "name": "mochawesome",
    "nyc": {
        "include": [
            "src/*.js"
        ],
        "require": [
            "babel-register"
        ],
        "sourceMap": false,
        "instrument": false,
        "reporter": [
            "lcov",
            "html",
            "text-summary"
        ],
        "cache": true,
        "check-coverage": true,
        "lines": 99,
        "statements": 99,
        "functions": 100,
        "branches": 90
    },
    "optionalDependencies": {},
    "peerDependencies": {
        "mocha": "*"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/adamgruber/mochawesome.git"
    },
    "scripts": {
        "build": "babel src -d dist",
        "lint": "eslint src test",
        "test": "npm run lint && cross-env NODE_ENV=test nyc mocha",
        "test:ctx": "mocha test-functional/test-context.js --opts test-functional/mocha.opts",
        "test:fn": "mocha test-functional/test.js --opts test-functional/mocha.opts",
        "test:mem": "mocha test-functional/mem-test.js --opts test-functional/mocha.opts"
    },
    "version": "2.0.5",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
