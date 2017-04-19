# npmdoc-sass-lint

#### api documentation for  [sass-lint (v1.10.2)](https://github.com/sasstools/sass-lint)  [![npm package](https://img.shields.io/npm/v/npmdoc-sass-lint.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sass-lint) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sass-lint.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sass-lint)

#### All Node Sass linter!

[![NPM](https://nodei.co/npm/sass-lint.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/sass-lint)

- [https://npmdoc.github.io/node-npmdoc-sass-lint/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-sass-lint/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sass-lint/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sass-lint/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-sass-lint/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-sass-lint/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Sam Richard"
    },
    "bin": {
        "sass-lint": "./bin/sass-lint.js"
    },
    "bugs": {
        "url": "https://github.com/sasstools/sass-lint/issues"
    },
    "dependencies": {
        "commander": "^2.8.1",
        "eslint": "^2.7.0",
        "front-matter": "2.1.0",
        "fs-extra": "^1.0.0",
        "glob": "^7.0.0",
        "globule": "^1.0.0",
        "gonzales-pe": "3.4.7",
        "js-yaml": "^3.5.4",
        "lodash.capitalize": "^4.1.0",
        "lodash.kebabcase": "^4.0.0",
        "merge": "^1.2.0",
        "path-is-absolute": "^1.0.0",
        "util": "^0.10.3"
    },
    "description": "All Node Sass linter!",
    "devDependencies": {
        "coveralls": "^2.11.4",
        "deep-equal": "^1.0.1",
        "istanbul": "^0.4.0",
        "mocha": "^3.0.1",
        "sinon": "^1.17.4"
    },
    "directories": {},
    "dist": {
        "shasum": "825bd6b0da79ddd36a42ffae5b6d44ac4922502b",
        "tarball": "https://registry.npmjs.org/sass-lint/-/sass-lint-1.10.2.tgz"
    },
    "gitHead": "f998ec700c8574cf3b85dcbc6fac558e5b0457e5",
    "homepage": "https://github.com/sasstools/sass-lint",
    "keywords": [
        "Sass",
        "SCSS",
        "lint"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "bgriffith"
        },
        {
            "name": "danpurdy"
        },
        {
            "name": "snugug"
        }
    ],
    "name": "sass-lint",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/sasstools/sass-lint.git"
    },
    "scripts": {
        "coveralls": "cat ./coverage/lcov.info | ./node_modules/coveralls/bin/coveralls.js",
        "pretest": "eslint .",
        "preversion": "npm test",
        "test": "istanbul cover ./node_modules/mocha/bin/_mocha --report lcovonly -- -R spec -t 3000 tests tests/rules tests/helpers"
    },
    "version": "1.10.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
