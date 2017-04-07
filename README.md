# api documentation for  [mochawesome (v2.0.4)](https://github.com/adamgruber/mochawesome#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-mochawesome.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mochawesome) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mochawesome.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mochawesome)
#### A Gorgeous HTML/CSS Reporter for Mocha.js

[![NPM](https://nodei.co/npm/mochawesome.png?downloads=true)](https://www.npmjs.com/package/mochawesome)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mochawesome/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-mochawesome_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mochawesome/build/apidoc.html)

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
        "shasum": "18c0ba1ce9db363c946618506bba1a73df6f4054",
        "tarball": "https://registry.npmjs.org/mochawesome/-/mochawesome-2.0.4.tgz"
    },
    "engine": "node >= 4",
    "gitHead": "5c04cc8b7e4e2599984cceea9a6de764d33b4b80",
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
            "name": "adamgruber",
            "email": "talknmime@gmail.com"
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
    "readme": "ERROR: No README data found!",
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
    "version": "2.0.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mochawesome](#apidoc.module.mochawesome)
1.  object <span class="apidocSignatureSpan">mochawesome.</span>utils

#### [module mochawesome.utils](#apidoc.module.mochawesome.utils)
1.  [function <span class="apidocSignatureSpan">mochawesome.utils.</span>cleanCode (str)](#apidoc.element.mochawesome.utils.cleanCode)
1.  [function <span class="apidocSignatureSpan">mochawesome.utils.</span>cleanSuite (suite, totalTestsRegistered)](#apidoc.element.mochawesome.utils.cleanSuite)
1.  [function <span class="apidocSignatureSpan">mochawesome.utils.</span>cleanTest (test)](#apidoc.element.mochawesome.utils.cleanTest)
1.  [function <span class="apidocSignatureSpan">mochawesome.utils.</span>getPercentClass (pct)](#apidoc.element.mochawesome.utils.getPercentClass)
1.  [function <span class="apidocSignatureSpan">mochawesome.utils.</span>log (msg, level, config)](#apidoc.element.mochawesome.utils.log)
1.  [function <span class="apidocSignatureSpan">mochawesome.utils.</span>removeAllPropsFromObjExcept (obj, propsToKeep)](#apidoc.element.mochawesome.utils.removeAllPropsFromObjExcept)
1.  [function <span class="apidocSignatureSpan">mochawesome.utils.</span>saveFile (filename, data)](#apidoc.element.mochawesome.utils.saveFile)
1.  [function <span class="apidocSignatureSpan">mochawesome.utils.</span>traverseSuites (suite, totalTestsRegistered)](#apidoc.element.mochawesome.utils.traverseSuites)



# <a name="apidoc.module.mochawesome"></a>[module mochawesome](#apidoc.module.mochawesome)



# <a name="apidoc.module.mochawesome.utils"></a>[module mochawesome.utils](#apidoc.module.mochawesome.utils)

#### <a name="apidoc.element.mochawesome.utils.cleanCode"></a>[function <span class="apidocSignatureSpan">mochawesome.utils.</span>cleanCode (str)](#apidoc.element.mochawesome.utils.cleanCode)
- description and source-code
```javascript
function cleanCode(str) {
  str = str
    .replace(/\r\n?|[\n\u2028\u2029]/g, '\n').replace(/^\uFEFF/, '')
    .replace(/^function\s*\(.*\)\s*{|\(.*\)\s*=>\s*{?/, '')
    .replace(/\s*\}$/, '');

  const spaces = str.match(/^\n?( *)/)[1].length;
  const tabs = str.match(/^\n?(\t*)/)[1].length;
<span class="apidocCodeCommentSpan">  /* istanbul ignore next */
</span>  const re = new RegExp('^\n?${tabs ? '\t' : ' '}{${tabs || spaces}}', 'gm');

  str = str.replace(re, '');
  str = str.replace(/^\s+|\s+$/g, '');
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mochawesome.utils.cleanSuite"></a>[function <span class="apidocSignatureSpan">mochawesome.utils.</span>cleanSuite (suite, totalTestsRegistered)](#apidoc.element.mochawesome.utils.cleanSuite)
- description and source-code
```javascript
function cleanSuite(suite, totalTestsRegistered) {
  // console.log(stringify(suite));
  suite.uuid = uuid.v4();

  const cleanTests = _.map(suite.tests, cleanTest);
  const passingTests = _.filter(cleanTests, { state: 'passed' });
  const failingTests = _.filter(cleanTests, { state: 'failed' });
  const pendingTests = _.filter(cleanTests, { pending: true });
  const skippedTests = _.filter(cleanTests, { skipped: true });
  let duration = 0;

  _.each(cleanTests, test => {
    duration += test.duration;
  });

  totalTestsRegistered.total += suite.tests.length;

  suite.tests = cleanTests;
  suite.fullFile = suite.file || '';
  suite.file = suite.file ? suite.file.replace(process.cwd(), '') : '';
  suite.passes = passingTests;
  suite.failures = failingTests;
  suite.pending = pendingTests;
  suite.skipped = skippedTests;
  suite.hasTests = suite.tests.length > 0;
  suite.hasSuites = suite.suites.length > 0;
  suite.totalTests = suite.tests.length;
  suite.totalPasses = passingTests.length;
  suite.totalFailures = failingTests.length;
  suite.totalPending = pendingTests.length;
  suite.totalSkipped = skippedTests.length;
  suite.hasPasses = passingTests.length > 0;
  suite.hasFailures = failingTests.length > 0;
  suite.hasPending = pendingTests.length > 0;
  suite.hasSkipped = suite.skipped.length > 0;
  suite.duration = duration;
  suite.rootEmpty = suite.root && suite.totalTests === 0;

  removeAllPropsFromObjExcept(suite, [
    'title',
    'fullFile',
    'file',
    'tests',
    'suites',
    'passes',
    'failures',
    'pending',
    'skipped',
    'hasTests',
    'hasSuites',
    'totalTests',
    'totalPasses',
    'totalFailures',
    'totalPending',
    'totalSkipped',
    'hasPasses',
    'hasFailures',
    'hasPending',
    'hasSkipped',
    'root',
    'uuid',
    'duration',
    'rootEmpty',
    '_timeout'
  ]);
  // console.log(suite.suites[0].tests);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mochawesome.utils.cleanTest"></a>[function <span class="apidocSignatureSpan">mochawesome.utils.</span>cleanTest (test)](#apidoc.element.mochawesome.utils.cleanTest)
- description and source-code
```javascript
function cleanTest(test) {
<span class="apidocCodeCommentSpan">  /**
   * Check that a / b have the same type.
   */
</span>  function sameType(a, b) {
    const objToString = Object.prototype.toString;
    return objToString.call(a) === objToString.call(b);
  }

  /* istanbul ignore next: test.fn exists prior to mocha 2.4.0 */
  let code = test.fn ? test.fn.toString() : test.body;
  const err = test.err || {};
  const { actual, expected, showDiff, stack } = err;

  if (code) {
    code = cleanCode(code);
  }

  if (stack) {
    err.estack = err.stack;
  }

  // Create diff for the error
  if (showDiff !== false && sameType(actual, expected) && expected !== undefined) {
    /* istanbul ignore if */
    if (!(_.isString(actual) && _.isString(expected))) {
      err.actual = mochaUtils.stringify(actual);
      err.expected = mochaUtils.stringify(expected);
    }
    err.diff = diff
      .createPatch('string', err.actual, err.expected)
      .split('\n')
      .splice(4)
      .map(line => {
        if (line.match(/@@/)) {
          return null;
        }
        if (line.match(/\\ No newline/)) {
          return null;
        }
        return line.replace(/^(-|\+)/, '$1 ');
      })
      .filter(line => typeof line !== 'undefined' && line !== null)
      .join('\n');
  }

  const cleaned = {
    title: test.title,
    fullTitle: _.isFunction(test.fullTitle) ? test.fullTitle() : /* istanbul ignore next */test.title,
    timedOut: test.timedOut,
    duration: test.duration || 0,
    state: test.state,
    speed: test.speed,
    pass: test.state === 'passed',
    fail: test.state === 'failed',
    pending: test.pending,
    context: stringify(test.context, null, 2),
    code,
    err,
    isRoot: test.parent && test.parent.root,
    uuid: test.uuid || /* istanbul ignore next: default */uuid.v4(),
    parentUUID: test.parent && test.parent.uuid
  };

  cleaned.skipped = (!cleaned.pass && !cleaned.fail && !cleaned.pending);

  return cleaned;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mochawesome.utils.getPercentClass"></a>[function <span class="apidocSignatureSpan">mochawesome.utils.</span>getPercentClass (pct)](#apidoc.element.mochawesome.utils.getPercentClass)
- description and source-code
```javascript
function getPercentClass(pct) {
  if (pct <= 50) {
    return 'danger';
  } else if (pct > 50 && pct < 80) {
    return 'warning';
  } else {
    return 'success';
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mochawesome.utils.log"></a>[function <span class="apidocSignatureSpan">mochawesome.utils.</span>log (msg, level, config)](#apidoc.element.mochawesome.utils.log)
- description and source-code
```javascript
function log(msg, level, config) {
  // Don't log messages in quiet mode
  if (config && config.quiet) return;
  const logMethod = console[level] || console.log;
  let out = msg;
  if (typeof msg === 'object') {
    out = stringify(msg, null, 2);
  }
  logMethod('[${chalk.gray('mochawesome')}] ${out}\n');
}
```
- example usage
```shell
...
 * the template and remove unused properties.
 *
 * @param {Object} suite
 * @param {Object} totalTestsRegistered
 * @param {Integer} totalTestsRegistered.total
 */
function cleanSuite(suite, totalTestsRegistered) {
// console.log(stringify(suite));
suite.uuid = uuid.v4();

const cleanTests = _.map(suite.tests, cleanTest);
const passingTests = _.filter(cleanTests, { state: 'passed' });
const failingTests = _.filter(cleanTests, { state: 'failed' });
const pendingTests = _.filter(cleanTests, { pending: true });
const skippedTests = _.filter(cleanTests, { skipped: true });
...
```

#### <a name="apidoc.element.mochawesome.utils.removeAllPropsFromObjExcept"></a>[function <span class="apidocSignatureSpan">mochawesome.utils.</span>removeAllPropsFromObjExcept (obj, propsToKeep)](#apidoc.element.mochawesome.utils.removeAllPropsFromObjExcept)
- description and source-code
```javascript
function removeAllPropsFromObjExcept(obj, propsToKeep) {
  _.forOwn(obj, (val, prop) => {
    if (propsToKeep.indexOf(prop) === -1) {
      delete obj[prop];
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mochawesome.utils.saveFile"></a>[function <span class="apidocSignatureSpan">mochawesome.utils.</span>saveFile (filename, data)](#apidoc.element.mochawesome.utils.saveFile)
- description and source-code
```javascript
function saveFile(filename, data) {
  return new Promise((resolve, reject) => {
    fs.outputFile(filename, data, err => err === null ? resolve(true) : reject(err));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mochawesome.utils.traverseSuites"></a>[function <span class="apidocSignatureSpan">mochawesome.utils.</span>traverseSuites (suite, totalTestsRegistered)](#apidoc.element.mochawesome.utils.traverseSuites)
- description and source-code
```javascript
function traverseSuites(suite, totalTestsRegistered) {
  const queue = [];
  let next = suite;
  while (next) {
    if (next.root) {
      cleanSuite(next, totalTestsRegistered);
    }
    if (next.suites.length) {
      _.each(next.suites, (nextSuite, i) => {
        cleanSuite(nextSuite, totalTestsRegistered);
        queue.push(nextSuite);
      });
    }
    next = queue.shift();
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
