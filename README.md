# api documentation for  [sass-lint (v1.10.2)](https://github.com/sasstools/sass-lint)  [![npm package](https://img.shields.io/npm/v/npmdoc-sass-lint.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sass-lint) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sass-lint.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sass-lint)
#### All Node Sass linter!

[![NPM](https://nodei.co/npm/sass-lint.png?downloads=true)](https://www.npmjs.com/package/sass-lint)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sass-lint/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-sass-lint_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sass-lint/build/apidoc.html)

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
            "name": "bgriffith",
            "email": "gt11687@gmail.com"
        },
        {
            "name": "danpurdy",
            "email": "danjpurdy@gmail.com"
        },
        {
            "name": "snugug",
            "email": "sam@snug.ug"
        }
    ],
    "name": "sass-lint",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module sass-lint](#apidoc.module.sass-lint)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>errorCount (results)](#apidoc.element.sass-lint.errorCount)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>failOnError (results, options, configPath)](#apidoc.element.sass-lint.failOnError)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>format (results, options, configPath)](#apidoc.element.sass-lint.format)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>getConfig (config, configPath)](#apidoc.element.sass-lint.getConfig)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>lintFileText (file, options, configPath)](#apidoc.element.sass-lint.lintFileText)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>lintFiles (files, options, configPath)](#apidoc.element.sass-lint.lintFiles)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>lintText (file, options, configPath)](#apidoc.element.sass-lint.lintText)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>outputResults (results, options, configPath)](#apidoc.element.sass-lint.outputResults)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>resultCount (results)](#apidoc.element.sass-lint.resultCount)
1.  [function <span class="apidocSignatureSpan">sass-lint.</span>warningCount (results)](#apidoc.element.sass-lint.warningCount)
1.  object <span class="apidocSignatureSpan">sass-lint.</span>config_helpers
1.  object <span class="apidocSignatureSpan">sass-lint.</span>exceptions
1.  object <span class="apidocSignatureSpan">sass-lint.</span>helpers
1.  object <span class="apidocSignatureSpan">sass-lint.</span>ruleToggler
1.  object <span class="apidocSignatureSpan">sass-lint.</span>selector_helpers

#### [module sass-lint.config_helpers](#apidoc.module.sass-lint.config_helpers)
1.  [function <span class="apidocSignatureSpan">sass-lint.config_helpers.</span>checkForConfigExtend (config, curConfPath)](#apidoc.element.sass-lint.config_helpers.checkForConfigExtend)
1.  [function <span class="apidocSignatureSpan">sass-lint.config_helpers.</span>findFile (configPath, filename)](#apidoc.element.sass-lint.config_helpers.findFile)
1.  [function <span class="apidocSignatureSpan">sass-lint.config_helpers.</span>loadConfig (cPath)](#apidoc.element.sass-lint.config_helpers.loadConfig)
1.  [function <span class="apidocSignatureSpan">sass-lint.config_helpers.</span>loadDefaults ()](#apidoc.element.sass-lint.config_helpers.loadDefaults)

#### [module sass-lint.exceptions](#apidoc.module.sass-lint.exceptions)
1.  [function <span class="apidocSignatureSpan">sass-lint.exceptions.</span>MaxWarningsExceededError (message)](#apidoc.element.sass-lint.exceptions.MaxWarningsExceededError)
1.  [function <span class="apidocSignatureSpan">sass-lint.exceptions.</span>SassLintFailureError (message)](#apidoc.element.sass-lint.exceptions.SassLintFailureError)

#### [module sass-lint.helpers](#apidoc.module.sass-lint.helpers)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>addUnique (results, item)](#apidoc.element.sass-lint.helpers.addUnique)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>attemptTraversal (node, traversalPath)](#apidoc.element.sass-lint.helpers.attemptTraversal)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>collectSuffixExtensions (ruleset, selectorType)](#apidoc.element.sass-lint.helpers.collectSuffixExtensions)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>hasEOL (str)](#apidoc.element.sass-lint.helpers.hasEOL)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isCamelCase (str)](#apidoc.element.sass-lint.helpers.isCamelCase)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isEmptyLine (str)](#apidoc.element.sass-lint.helpers.isEmptyLine)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isEqual (a, b)](#apidoc.element.sass-lint.helpers.isEqual)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isHyphenatedBEM (str)](#apidoc.element.sass-lint.helpers.isHyphenatedBEM)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isHyphenatedLowercase (str)](#apidoc.element.sass-lint.helpers.isHyphenatedLowercase)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isLowerCase (str)](#apidoc.element.sass-lint.helpers.isLowerCase)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isNestable (currentVal, previousVal, elements, nestable)](#apidoc.element.sass-lint.helpers.isNestable)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isNewLine (node)](#apidoc.element.sass-lint.helpers.isNewLine)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isNumber (val)](#apidoc.element.sass-lint.helpers.isNumber)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isPartialStringMatch (needle, haystack)](#apidoc.element.sass-lint.helpers.isPartialStringMatch)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isPascalCase (str)](#apidoc.element.sass-lint.helpers.isPascalCase)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isSnakeCase (str)](#apidoc.element.sass-lint.helpers.isSnakeCase)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isSpace (node)](#apidoc.element.sass-lint.helpers.isSpace)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isStrictBEM (str)](#apidoc.element.sass-lint.helpers.isStrictBEM)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isUnique (results, item)](#apidoc.element.sass-lint.helpers.isUnique)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isUpperCase (str)](#apidoc.element.sass-lint.helpers.isUpperCase)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isValidHex (str)](#apidoc.element.sass-lint.helpers.isValidHex)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>loadConfigFile (configPath)](#apidoc.element.sass-lint.helpers.loadConfigFile)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>log (input)](#apidoc.element.sass-lint.helpers.log)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>propertySearch (haystack, needle, property)](#apidoc.element.sass-lint.helpers.propertySearch)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>sortDetects (a, b)](#apidoc.element.sass-lint.helpers.sortDetects)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>stripBom (str)](#apidoc.element.sass-lint.helpers.stripBom)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>stripLastSpace (selector)](#apidoc.element.sass-lint.helpers.stripLastSpace)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>stripPrefix (str)](#apidoc.element.sass-lint.helpers.stripPrefix)
1.  [function <span class="apidocSignatureSpan">sass-lint.helpers.</span>stripQuotes (str)](#apidoc.element.sass-lint.helpers.stripQuotes)

#### [module sass-lint.ruleToggler](#apidoc.module.sass-lint.ruleToggler)
1.  [function <span class="apidocSignatureSpan">sass-lint.ruleToggler.</span>getToggledRules (ast)](#apidoc.element.sass-lint.ruleToggler.getToggledRules)
1.  [function <span class="apidocSignatureSpan">sass-lint.ruleToggler.</span>isResultEnabled (toggledRules)](#apidoc.element.sass-lint.ruleToggler.isResultEnabled)

#### [module sass-lint.selector_helpers](#apidoc.module.sass-lint.selector_helpers)
1.  [function <span class="apidocSignatureSpan">sass-lint.selector_helpers.</span>constructSelector (val)](#apidoc.element.sass-lint.selector_helpers.constructSelector)



# <a name="apidoc.module.sass-lint"></a>[module sass-lint](#apidoc.module.sass-lint)

#### <a name="apidoc.element.sass-lint.errorCount"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>errorCount (results)](#apidoc.element.sass-lint.errorCount)
- description and source-code
```javascript
errorCount = function (results) {
  var errors = {
    count: 0,
    files: []
  };

  results.forEach(function (result) {
    if (result.errorCount) {
      errors.count += result.errorCount;
      errors.files.push(result.filePath);
    }
  });

  return errors;
}
```
- example usage
```shell
...
* a cumulative count of both
*
* @param {object} results our results object
* @returns {int} the cumulative count of errors and warnings detected
*/
sassLint.resultCount = function (results) {
 var warnings = this.warningCount(results),
     errors = this.errorCount(results);

 return warnings.count + errors.count;
};

/**
* Runs each rule against our AST tree and returns our main object of detected
* errors, warnings, messages and filenames.
...
```

#### <a name="apidoc.element.sass-lint.failOnError"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>failOnError (results, options, configPath)](#apidoc.element.sass-lint.failOnError)
- description and source-code
```javascript
failOnError = function (results, options, configPath) {
  // Default parameters
  options = typeof options !== 'undefined' ? options : {};
  configPath = typeof configPath !== 'undefined' ? configPath : null;

  var errorCount = this.errorCount(results),
      warningCount = this.warningCount(results),
      configOptions = this.getConfig(options, configPath).options;

  if (errorCount.count > 0) {
    throw new exceptions.SassLintFailureError(errorCount.count + ' errors were detected in \n- ' + errorCount.files.join('\n- '));
  }

  if (!isNaN(configOptions['max-warnings']) && warningCount.count > configOptions['max-warnings']) {
    throw new exceptions.MaxWarningsExceededError(
      'Number of warnings (' + warningCount.count +
      ') exceeds the allowed maximum of ' + configOptions['max-warnings'] +
      '.\n'
    );
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.format"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>format (results, options, configPath)](#apidoc.element.sass-lint.format)
- description and source-code
```javascript
format = function (results, options, configPath) {
  var config = this.getConfig(options, configPath),
      format = config.options.formatter.toLowerCase();

  var formatted = require('eslint/lib/formatters/' + format);

  return formatted(results);
}
```
- example usage
```shell
...
 * @returns {object} results our results object
 */
sassLint.outputResults = function (results, options, configPath) {
  var config = this.getConfig(options, configPath);

  if (this.resultCount(results)) {

var formatted = this.format(results, options, configPath);

if (config.options['output-file']) {
  try {
    fs.outputFileSync(path.resolve(process.cwd(), config.options['output-file']), formatted);
    console.log('Output successfully written to ' + path.resolve(process.cwd(), config.options['output-file']));
  }
  catch (e) {
...
```

#### <a name="apidoc.element.sass-lint.getConfig"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>getConfig (config, configPath)](#apidoc.element.sass-lint.getConfig)
- description and source-code
```javascript
getConfig = function (config, configPath) {
  return slConfig(config, configPath);
}
```
- example usage
```shell
...
 *
 * @param {object} file file object from fs.readFileSync
 * @param {object} options user specified rules/options passed in
 * @param {string} configPath path to a config file
 * @returns {object} an object containing error & warning counts plus lint messages for each parsed file
 */
sassLint.lintText = function (file, options, configPath) {
var rules = slRules(this.getConfig(options, configPath)),
    ast = {},
    detects,
    results = [],
    errors = 0,
    warnings = 0,
    ruleToggles = null,
    isEnabledFilter = null;
...
```

#### <a name="apidoc.element.sass-lint.lintFileText"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>lintFileText (file, options, configPath)](#apidoc.element.sass-lint.lintFileText)
- description and source-code
```javascript
lintFileText = function (file, options, configPath) {
  var config = this.getConfig(options, configPath),
      ignores = config.files ? config.files.ignore : [];

  if (!globule.isMatch(ignores, file.filename)) {
    return this.lintText(file, options, configPath);
  }

  return {
    'filePath': file.filename,
    'warningCount': 0,
    'errorCount': 0,
    'messages': []
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.lintFiles"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>lintFiles (files, options, configPath)](#apidoc.element.sass-lint.lintFiles)
- description and source-code
```javascript
lintFiles = function (files, options, configPath) {
  var that = this,
      results = [],
      includes = [],
      ignores = '';

  // Files passed as a string on the command line
  if (files) {
    ignores = this.getConfig(options, configPath).files.ignore || '';
    if (files.indexOf(', ') !== -1) {
      files.split(', ').forEach(function (pattern) {
        includes = includes.concat(glob.sync(pattern, {ignore: ignores, nodir: true}));
      });
    }
    else {
      includes = glob.sync(files, {ignore: ignores, nodir: true});
    }
  }
  // If not passed in then we look in the config file
  else {
    files = this.getConfig(options, configPath).files;
    // A glob pattern of files can be just a string
    if (typeof files === 'string') {
      includes = glob.sync(files, {nodir: true});
    }
    // Look into the include property of files and check if there's an array of files
    else if (files.include && files.include instanceof Array) {
      files.include.forEach(function (pattern) {
        includes = includes.concat(glob.sync(pattern, {ignore: files.ignore, nodir: true}));
      });
    }
    // Or there is only one pattern in the include property of files
    else {
      includes = glob.sync(files.include, {ignore: files.ignore, nodir: true});
    }
  }

  includes.forEach(function (file, index) {
    // Only lint non duplicate files from our glob results
    if (includes.indexOf(file) === index) {
      var lint = that.lintText({
        'text': fs.readFileSync(file),
        'format': options.syntax ? options.syntax : path.extname(file).replace('.', ''),
        'filename': file
      }, options, configPath);
      results.push(lint);
    }
  });

  return results;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.lintText"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>lintText (file, options, configPath)](#apidoc.element.sass-lint.lintText)
- description and source-code
```javascript
lintText = function (file, options, configPath) {
  var rules = slRules(this.getConfig(options, configPath)),
      ast = {},
      detects,
      results = [],
      errors = 0,
      warnings = 0,
      ruleToggles = null,
      isEnabledFilter = null;

  try {
    ast = groot(file.text, file.format, file.filename);
  }
  catch (e) {
    var line = e.line || 1;
    errors++;

    results = [{
      ruleId: 'Fatal',
      line: line,
      column: 1,
      message: e.message,
      severity: 2
    }];
  }

  if (ast.content && ast.content.length > 0) {
    ruleToggles = getToggledRules(ast);
    isEnabledFilter = isResultEnabled(ruleToggles);

    rules.forEach(function (rule) {
      detects = rule.rule.detect(ast, rule)
        .filter(isEnabledFilter);
      results = results.concat(detects);
      if (detects.length) {
        if (rule.severity === 1) {
          warnings += detects.length;
        }
        else if (rule.severity === 2) {
          errors += detects.length;
        }
      }
    });
  }

  results.sort(helpers.sortDetects);

  return {
    'filePath': file.filename,
    'warningCount': warnings,
    'errorCount': errors,
    'messages': results
  };
}
```
- example usage
```shell
...
 * @returns {object} Return the results of lintText - a results object
 */
sassLint.lintFileText = function (file, options, configPath) {
var config = this.getConfig(options, configPath),
    ignores = config.files ? config.files.ignore : [];

if (!globule.isMatch(ignores, file.filename)) {
  return this.lintText(file, options, configPath);
}

return {
  'filePath': file.filename,
  'warningCount': 0,
  'errorCount': 0,
  'messages': []
...
```

#### <a name="apidoc.element.sass-lint.outputResults"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>outputResults (results, options, configPath)](#apidoc.element.sass-lint.outputResults)
- description and source-code
```javascript
outputResults = function (results, options, configPath) {
  var config = this.getConfig(options, configPath);

  if (this.resultCount(results)) {

    var formatted = this.format(results, options, configPath);

    if (config.options['output-file']) {
      try {
        fs.outputFileSync(path.resolve(process.cwd(), config.options['output-file']), formatted);
        console.log('Output successfully written to ' + path.resolve(process.cwd(), config.options['output-file']));
      }
      catch (e) {
        console.log('Error: Output was unable to be written to ' + path.resolve(process.cwd(), config.options['output-file']));
      }
    }
    else {
      console.log(formatted);
    }
  }
  return results;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.resultCount"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>resultCount (results)](#apidoc.element.sass-lint.resultCount)
- description and source-code
```javascript
resultCount = function (results) {
  var warnings = this.warningCount(results),
      errors = this.errorCount(results);

  return warnings.count + errors.count;
}
```
- example usage
```shell
...
 * @param {object} options user specified rules/options passed in
 * @param {string} configPath path to a config file
 * @returns {object} results our results object
 */
sassLint.outputResults = function (results, options, configPath) {
  var config = this.getConfig(options, configPath);

  if (this.resultCount(results)) {

var formatted = this.format(results, options, configPath);

if (config.options['output-file']) {
  try {
    fs.outputFileSync(path.resolve(process.cwd(), config.options['output-file']), formatted);
    console.log('Output successfully written to ' + path.resolve(process.cwd(), config.options['output-file']));
...
```

#### <a name="apidoc.element.sass-lint.warningCount"></a>[function <span class="apidocSignatureSpan">sass-lint.</span>warningCount (results)](#apidoc.element.sass-lint.warningCount)
- description and source-code
```javascript
warningCount = function (results) {
  var warnings = {
    count: 0,
    files: []
  };

  results.forEach(function (result) {
    if (result.warningCount) {
      warnings.count += result.warningCount;
      warnings.files.push(result.filePath);
    }
  });

  return warnings;
}
```
- example usage
```shell
...
* Parses our results object to count warnings and errors and return
* a cumulative count of both
*
* @param {object} results our results object
* @returns {int} the cumulative count of errors and warnings detected
*/
sassLint.resultCount = function (results) {
 var warnings = this.warningCount(results),
     errors = this.errorCount(results);

 return warnings.count + errors.count;
};

/**
* Runs each rule against our AST tree and returns our main object of detected
...
```



# <a name="apidoc.module.sass-lint.config_helpers"></a>[module sass-lint.config_helpers](#apidoc.module.sass-lint.config_helpers)

#### <a name="apidoc.element.sass-lint.config_helpers.checkForConfigExtend"></a>[function <span class="apidocSignatureSpan">sass-lint.config_helpers.</span>checkForConfigExtend (config, curConfPath)](#apidoc.element.sass-lint.config_helpers.checkForConfigExtend)
- description and source-code
```javascript
checkForConfigExtend = function (config, curConfPath) {
  var mergedConfig = config,
      subConfig = config.options['config-file'] || false,
      confPath,
      resolvedSubConfig;

  if (subConfig) {
    if (!pathIsAbsolute(subConfig)) {
      // Process.cwd() in most IDE's will be / so therefore we need to pass the current directory
      // of the config from which you are 'extending' or we resort to process.cwd() which on the CLI
      // will be correct
      confPath = curConfPath ? path.dirname(curConfPath) : process.cwd();
      subConfig = path.resolve(confPath, subConfig);
    }
    // Attempt to load the new found config file
    resolvedSubConfig = loadConfig(subConfig, curConfPath);
    // Check the new config file to see if it too is extending
    resolvedSubConfig = checkForConfigExtend(resolvedSubConfig, subConfig);
    // Merge our configs with the first encountered being the most important, down to the last config
    // being the least.
    mergedConfig = merge.recursive(resolvedSubConfig, config);
  }

  return mergedConfig;
}
```
- example usage
```shell
...
  }
}
else if (!pathIsAbsolute(configPath)) {
  configPath = path.resolve(process.cwd(), configPath);
}

config = confHelpers.loadConfig(configPath);
config = confHelpers.checkForConfigExtend(config, configPath);

// check to see if user config contains an options property and whether property has a property called merge-default-rules
configMergeExists = (config.options && typeof config.options['merge-default-rules'] !== 'undefined');

// If it does then retrieve the value of it here or return false
configMerge = configMergeExists ? config.options['merge-default-rules'] : false;
...
```

#### <a name="apidoc.element.sass-lint.config_helpers.findFile"></a>[function <span class="apidocSignatureSpan">sass-lint.config_helpers.</span>findFile (configPath, filename)](#apidoc.element.sass-lint.config_helpers.findFile)
- description and source-code
```javascript
function findFile(configPath, filename) {
  var HOME = process.env.HOME || process.env.HOMEPATH || process.env.USERPROFILE,
      dirname = null,
      parentDirname = null;

  configPath = configPath || path.join(process.cwd(), filename);

  if (configPath && fs.existsSync(configPath)) {
    return fs.realpathSync(configPath);
  }
  dirname = path.dirname(configPath);
  parentDirname = path.dirname(dirname);

  if (dirname === null || dirname === HOME || dirname === parentDirname) {
    return null;
  }
  configPath = path.join(parentDirname, filename);

  return findFile(configPath, filename);
}
```
- example usage
```shell
...
  }

  if (options.options && options.options['config-file']) {
configPath = options.options['config-file'];
  }

  if (!configPath) {
metaPath = confHelpers.findFile(false, 'package.json');
if (metaPath) {
  meta = require(metaPath);
}

if (meta && meta.sasslintConfig) {
  configPath = path.resolve(path.dirname(metaPath), meta.sasslintConfig);
}
...
```

#### <a name="apidoc.element.sass-lint.config_helpers.loadConfig"></a>[function <span class="apidocSignatureSpan">sass-lint.config_helpers.</span>loadConfig (cPath)](#apidoc.element.sass-lint.config_helpers.loadConfig)
- description and source-code
```javascript
loadConfig = function (cPath) {
  var configPath = cPath,
      resolvedConfig = {};

  if (configPath) {
    if (fs.existsSync(configPath)) {
      resolvedConfig = yaml.safeLoad(fs.readFileSync(configPath, 'utf8')) || {};
    }
  }

  return {
    options: resolvedConfig.options || {},
    files: resolvedConfig.files || {},
    rules: resolvedConfig.rules || {}
  };
}
```
- example usage
```shell
...
    configPath = confHelpers.findFile(false, '.sass-lint.yml');
  }
}
else if (!pathIsAbsolute(configPath)) {
  configPath = path.resolve(process.cwd(), configPath);
}

config = confHelpers.loadConfig(configPath);
config = confHelpers.checkForConfigExtend(config, configPath);

// check to see if user config contains an options property and whether property has a property called merge-default-rules
configMergeExists = (config.options && typeof config.options['merge-default-rules'] !== 'undefined');

// If it does then retrieve the value of it here or return false
configMerge = configMergeExists ? config.options['merge-default-rules'] : false;
...
```

#### <a name="apidoc.element.sass-lint.config_helpers.loadDefaults"></a>[function <span class="apidocSignatureSpan">sass-lint.config_helpers.</span>loadDefaults ()](#apidoc.element.sass-lint.config_helpers.loadDefaults)
- description and source-code
```javascript
function loadDefaults() {
  return yaml.safeLoad(fs.readFileSync(path.join(__dirname, 'config', 'sass-lint.yml'), 'utf8'));
}
```
- example usage
```shell
...
// If it does then retrieve the value of it here or return false
optionsMerge = optionsMergeExists ? options.options['merge-default-rules'] : false;


// order of preference is inline options > user config > default config
// merge-default-rules defaults to true so each step above should merge with the previous. If at any step merge-default-rules is
 set to
// false it should skip that steps merge.
defaults = confHelpers.loadDefaults();
finalConfig = merge.recursive(defaults, config, options);

// if merge-default-rules is set to false in user config file then we essentially skip the merging with default rules by overwriting
 our
// final rules with the content of our user config otherwise we don't take action here as the default merging has already happened
if (configMergeExists && !configMerge) {
  finalConfig.rules = config.rules;
}
...
```



# <a name="apidoc.module.sass-lint.exceptions"></a>[module sass-lint.exceptions](#apidoc.module.sass-lint.exceptions)

#### <a name="apidoc.element.sass-lint.exceptions.MaxWarningsExceededError"></a>[function <span class="apidocSignatureSpan">sass-lint.exceptions.</span>MaxWarningsExceededError (message)](#apidoc.element.sass-lint.exceptions.MaxWarningsExceededError)
- description and source-code
```javascript
MaxWarningsExceededError = function (message) {
  Error.captureStackTrace(this, this.constructor);
  this.name = 'MaxWarningsExceededError';
  this.message = message;
}
```
- example usage
```shell
...
      configOptions = this.getConfig(options, configPath).options;

  if (errorCount.count > 0) {
    throw new exceptions.SassLintFailureError(errorCount.count + ' errors were detected in \n- ' + errorCount.files.join('\n- '));
  }

  if (!isNaN(configOptions['max-warnings']) && warningCount.count > configOptions['max-warnings']) {
    throw new exceptions.MaxWarningsExceededError(
      'Number of warnings (' + warningCount.count +
      ') exceeds the allowed maximum of ' + configOptions['max-warnings'] +
      '.\n'
    );
  }
};
...
```

#### <a name="apidoc.element.sass-lint.exceptions.SassLintFailureError"></a>[function <span class="apidocSignatureSpan">sass-lint.exceptions.</span>SassLintFailureError (message)](#apidoc.element.sass-lint.exceptions.SassLintFailureError)
- description and source-code
```javascript
SassLintFailureError = function (message) {
  Error.captureStackTrace(this, this.constructor);
  this.name = 'SassLintFailureError';
  this.message = message;
}
```
- example usage
```shell
...
configPath = typeof configPath !== 'undefined' ? configPath : null;

var errorCount = this.errorCount(results),
    warningCount = this.warningCount(results),
    configOptions = this.getConfig(options, configPath).options;

if (errorCount.count > 0) {
  throw new exceptions.SassLintFailureError(errorCount.count + ' errors were detected in \n- ' + errorCount.files.join('\n- '));
}

if (!isNaN(configOptions['max-warnings']) && warningCount.count > configOptions['max-warnings']) {
  throw new exceptions.MaxWarningsExceededError(
    'Number of warnings (' + warningCount.count +
    ') exceeds the allowed maximum of ' + configOptions['max-warnings'] +
    '.\n'
...
```



# <a name="apidoc.module.sass-lint.helpers"></a>[module sass-lint.helpers](#apidoc.module.sass-lint.helpers)

#### <a name="apidoc.element.sass-lint.helpers.addUnique"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>addUnique (results, item)](#apidoc.element.sass-lint.helpers.addUnique)
- description and source-code
```javascript
addUnique = function (results, item) {
  if (this.isUnique(results, item)) {
    results.push(item);
  }
  return results;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.attemptTraversal"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>attemptTraversal (node, traversalPath)](#apidoc.element.sass-lint.helpers.attemptTraversal)
- description and source-code
```javascript
attemptTraversal = function (node, traversalPath) {
  var i,
      nextNodeList,
      currentNodeList = [],
      processChildNode = function processChildNode (child) {
        child.forEach(traversalPath[i], function (n) {
          nextNodeList.push(n);
        });
      };

  node.forEach(traversalPath[0], function (n) {
    currentNodeList.push(n);
  });

  for (i = 1; i < traversalPath.length; i++) {
    if (currentNodeList.length === 0) {
      return [];
    }

    nextNodeList = [];
    currentNodeList.forEach(processChildNode);
    currentNodeList = nextNodeList;
  }
  return currentNodeList;
}
```
- example usage
```shell
...
 * Collects all suffix extensions for a selector
 * @param   {object}  ruleset      ASTNode of type ruleset, containing a selector with nested suffix extensions
 * @param   {string}  selectorType Node type of the selector (e.g. class, id)
 * @returns {array}                Array of Nodes with the content property replaced by the complete selector
 *                                       (without '.', '#', etc) resulting from suffix extensions
 */
helpers.collectSuffixExtensions = function (ruleset, selectorType) {
var parentSelectors = helpers.attemptTraversal(ruleset, ['selector', selectorType, 'ident']),
    childSuffixes = helpers.attemptTraversal(ruleset, ['block', 'ruleset']),
    selectorList = [];

if (parentSelectors.length === 0) {
  return [];
}
...
```

#### <a name="apidoc.element.sass-lint.helpers.collectSuffixExtensions"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>collectSuffixExtensions (ruleset, selectorType)](#apidoc.element.sass-lint.helpers.collectSuffixExtensions)
- description and source-code
```javascript
collectSuffixExtensions = function (ruleset, selectorType) {
  var parentSelectors = helpers.attemptTraversal(ruleset, ['selector', selectorType, 'ident']),
      childSuffixes = helpers.attemptTraversal(ruleset, ['block', 'ruleset']),
      selectorList = [];

  if (parentSelectors.length === 0) {
    return [];
  }

  // Goes recursively through all nodes that look like suffix extensions. There may be multiple parents that are
  // extended, so lots of looping is required.
  var processChildSuffix = function (child, parents) {
    var currentParents = [],
        selectors = helpers.attemptTraversal(child, ['selector', 'parentSelectorExtension', 'ident']),
        nestedChildSuffixes = helpers.attemptTraversal(child, ['block', 'ruleset']);

    selectors.forEach(function (childSuffixNode) {
      // append suffix extension to all parent selectors
      parents.forEach(function (parent) {
        // clone so we don't modify the actual AST
        var clonedChildSuffixNode = gonzales.createNode(childSuffixNode);
        clonedChildSuffixNode.content = parent.content + clonedChildSuffixNode.content;

        currentParents.push(clonedChildSuffixNode);
      });
    });

    selectorList = selectorList.concat(currentParents);

    nestedChildSuffixes.forEach(function (childSuffix) {
      processChildSuffix(childSuffix, currentParents);
    });
  };

  childSuffixes.forEach(function (childSuffix) {
    processChildSuffix(childSuffix, parentSelectors);
  });

  return parentSelectors.concat(selectorList);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.hasEOL"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>hasEOL (str)](#apidoc.element.sass-lint.helpers.hasEOL)
- description and source-code
```javascript
hasEOL = function (str) {
  return /\r\n|\n/.test(str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isCamelCase"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isCamelCase (str)](#apidoc.element.sass-lint.helpers.isCamelCase)
- description and source-code
```javascript
isCamelCase = function (str) {
  return /^[a-z][a-zA-Z0-9]*$/.test(str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isEmptyLine"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isEmptyLine (str)](#apidoc.element.sass-lint.helpers.isEmptyLine)
- description and source-code
```javascript
isEmptyLine = function (str) {
  return /(\r\n|\n){2}/.test(str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isEqual"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isEqual (a, b)](#apidoc.element.sass-lint.helpers.isEqual)
- description and source-code
```javascript
isEqual = function (a, b) {
  var startLine = a.start.line === b.start.line ? true : false,
      endLine = a.end.line === b.end.line ? true : false,
      type = a.type === b.type ? true : false,
      length = a.content.length === b.content.length ? true : false;

  if (startLine && endLine && type && length) {
    return true;
  }
  else {
    return false;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isHyphenatedBEM"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isHyphenatedBEM (str)](#apidoc.element.sass-lint.helpers.isHyphenatedBEM)
- description and source-code
```javascript
isHyphenatedBEM = function (str) {
  return !(/[A-Z]|-{3}|_{3}|[^_]_[^_]/.test(str));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isHyphenatedLowercase"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isHyphenatedLowercase (str)](#apidoc.element.sass-lint.helpers.isHyphenatedLowercase)
- description and source-code
```javascript
isHyphenatedLowercase = function (str) {
  return !(/[^\-a-z0-9]/.test(str));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isLowerCase"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isLowerCase (str)](#apidoc.element.sass-lint.helpers.isLowerCase)
- description and source-code
```javascript
isLowerCase = function (str) {
  var pieces = str.split(''),
      i,
      result = 0;

  for (i = 0; i < pieces.length; i++) {
    if (!helpers.isNumber(pieces[i])) {
      if (pieces[i] === pieces[i].toLowerCase() && pieces[i] !== pieces[i].toUpperCase()) {
        result++;
      }
      else {
        return false;
      }
    }
  }
  if (result) {
    return true;
  }
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isNestable"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isNestable (currentVal, previousVal, elements, nestable)](#apidoc.element.sass-lint.helpers.isNestable)
- description and source-code
```javascript
isNestable = function (currentVal, previousVal, elements, nestable) {
  // check if they are nestable by checking the previous element against one
  // of the user specified selector types
  if (elements.indexOf(previousVal) !== -1 && nestable.indexOf(currentVal) !== -1) {
    return true;
  }

  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isNewLine"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isNewLine (node)](#apidoc.element.sass-lint.helpers.isNewLine)
- description and source-code
```javascript
isNewLine = function (node) {
  // using type === instead of is just in case node happens to be a string
  return !!(node && node.type === 'space' && node.content.match('\n'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isNumber"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isNumber (val)](#apidoc.element.sass-lint.helpers.isNumber)
- description and source-code
```javascript
isNumber = function (val) {
  if (isNaN(parseInt(val, 10))) {
    return false;
  }
  return true;
}
```
- example usage
```shell
...

helpers.isUpperCase = function (str) {
var pieces = str.split(''),
    i,
    result = 0;

for (i = 0; i < pieces.length; i++) {
  if (!helpers.isNumber(pieces[i])) {
    if (pieces[i] === pieces[i].toUpperCase() && pieces[i] !== pieces[i].toLowerCase()) {
      result++;
    }
    else {
      return false;
    }
  }
...
```

#### <a name="apidoc.element.sass-lint.helpers.isPartialStringMatch"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isPartialStringMatch (needle, haystack)](#apidoc.element.sass-lint.helpers.isPartialStringMatch)
- description and source-code
```javascript
isPartialStringMatch = function (needle, haystack) {
  for (var i = 0; i < haystack.length; i++) {
    if (haystack[i].indexOf(needle) >= 0) {
      return true;
    }
  }

  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isPascalCase"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isPascalCase (str)](#apidoc.element.sass-lint.helpers.isPascalCase)
- description and source-code
```javascript
isPascalCase = function (str) {
  return /^[A-Z][a-zA-Z0-9]*$/.test(str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isSnakeCase"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isSnakeCase (str)](#apidoc.element.sass-lint.helpers.isSnakeCase)
- description and source-code
```javascript
isSnakeCase = function (str) {
  return !(/[^_a-z0-9]/.test(str));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isSpace"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isSpace (node)](#apidoc.element.sass-lint.helpers.isSpace)
- description and source-code
```javascript
isSpace = function (node) {
  return !!(node && node.type === 'space' && !node.content.match('\n'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isStrictBEM"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isStrictBEM (str)](#apidoc.element.sass-lint.helpers.isStrictBEM)
- description and source-code
```javascript
isStrictBEM = function (str) {
  return /^[a-z](\-?[a-z0-9]+)*(__[a-z0-9](\-?[a-z0-9]+)*)?((_[a-z0-9](\-?[a-z0-9]+)*){0,2})?$/.test(str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isUnique"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isUnique (results, item)](#apidoc.element.sass-lint.helpers.isUnique)
- description and source-code
```javascript
isUnique = function (results, item) {
  var search = this.propertySearch(results, item.line, 'line');

  if (search === -1) {
    return true;
  }
  else if (results[search].column === item.column && results[search].message === item.message) {
    return false;
  }
  else {
    return true;
  }
}
```
- example usage
```shell
...
}
else {
  return true;
}
};

helpers.addUnique = function (results, item) {
if (this.isUnique(results, item)) {
  results.push(item);
}
return results;
};

helpers.sortDetects = function (a, b) {
if (a.line < b.line) {
...
```

#### <a name="apidoc.element.sass-lint.helpers.isUpperCase"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isUpperCase (str)](#apidoc.element.sass-lint.helpers.isUpperCase)
- description and source-code
```javascript
isUpperCase = function (str) {
  var pieces = str.split(''),
      i,
      result = 0;

  for (i = 0; i < pieces.length; i++) {
    if (!helpers.isNumber(pieces[i])) {
      if (pieces[i] === pieces[i].toUpperCase() && pieces[i] !== pieces[i].toLowerCase()) {
        result++;
      }
      else {
        return false;
      }
    }
  }
  if (result) {
    return true;
  }
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.isValidHex"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>isValidHex (str)](#apidoc.element.sass-lint.helpers.isValidHex)
- description and source-code
```javascript
isValidHex = function (str) {
  if (str.match(/^([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})$/)) {
    return true;
  }
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.loadConfigFile"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>loadConfigFile (configPath)](#apidoc.element.sass-lint.helpers.loadConfigFile)
- description and source-code
```javascript
loadConfigFile = function (configPath) {
  var fileDir = path.dirname(configPath),
      fileName = path.basename(configPath),
      fileExtension = path.extname(fileName),
      filePath = path.join(__dirname, 'config', fileDir, fileName),
      file = fs.readFileSync(filePath, 'utf8') || false;

  if (file) {
    if (fileExtension === '.yml') {
      return yaml.safeLoad(file);
    }
  }

  return file;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.log"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>log (input)](#apidoc.element.sass-lint.helpers.log)
- description and source-code
```javascript
function log(input) {
  console.log(util.inspect(input, false, null));
}
```
- example usage
```shell
...
  if (this.resultCount(results)) {

var formatted = this.format(results, options, configPath);

if (config.options['output-file']) {
  try {
    fs.outputFileSync(path.resolve(process.cwd(), config.options['output-file']), formatted);
    console.log('Output successfully written to ' + path.resolve(process.cwd(), config.options['output-file']));
  }
  catch (e) {
    console.log('Error: Output was unable to be written to ' + path.resolve(process.cwd(), config.options['output-file']));
  }
}
else {
  console.log(formatted);
...
```

#### <a name="apidoc.element.sass-lint.helpers.propertySearch"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>propertySearch (haystack, needle, property)](#apidoc.element.sass-lint.helpers.propertySearch)
- description and source-code
```javascript
propertySearch = function (haystack, needle, property) {
  var length = haystack.length,
      i;

  for (i = 0; i < length; i++) {
    if (haystack[i][property] === needle) {
      return i;
    }
  }
  return -1;
}
```
- example usage
```shell
...
}
else {
  return false;
}
};

helpers.isUnique = function (results, item) {
var search = this.propertySearch(results, item.line, 'line');

if (search === -1) {
  return true;
}
else if (results[search].column === item.column && results[search].message === item.message) {
  return false;
}
...
```

#### <a name="apidoc.element.sass-lint.helpers.sortDetects"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>sortDetects (a, b)](#apidoc.element.sass-lint.helpers.sortDetects)
- description and source-code
```javascript
sortDetects = function (a, b) {
  if (a.line < b.line) {
    return -1;
  }
  if (a.line > b.line) {
    return 1;
  }
  if (a.line === b.line) {
    if (a.column < b.column) {
      return -1;
    }
    if (a.column > b.column) {
      return 1;
    }
    return 0;
  }
  return 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.stripBom"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>stripBom (str)](#apidoc.element.sass-lint.helpers.stripBom)
- description and source-code
```javascript
stripBom = function (str) {
  if (typeof str !== 'string') {
    throw new TypeError('Expected a string, got ' + typeof str);
  }

  if (str.charCodeAt(0) === 0xFEFF) {
    return str.slice(1);
  }

  return str;
}
```
- example usage
```shell
...
var fm = require('front-matter');
var helpers = require('./helpers');

module.exports = function (text, syntax, filename) {
var tree;

// Run '.toString()' to allow Buffers to be passed in
text = helpers.stripBom(text.toString());

// if we're skipping front matter do it here, fall back to just our text in case it fails
if (fm.test(text)) {
  text = fm(text).body || text;
}

try {
...
```

#### <a name="apidoc.element.sass-lint.helpers.stripLastSpace"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>stripLastSpace (selector)](#apidoc.element.sass-lint.helpers.stripLastSpace)
- description and source-code
```javascript
stripLastSpace = function (selector) {

  if (selector.charAt(selector.length - 1) === ' ') {
    return selector.substr(0, selector.length - 1);

  }

  return selector;

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.stripPrefix"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>stripPrefix (str)](#apidoc.element.sass-lint.helpers.stripPrefix)
- description and source-code
```javascript
stripPrefix = function (str) {
  var modPropertyArr = str.split('-'),
      modProperty = '',
      prefLength = modPropertyArr[2] === 'osx' ? 2 : 1;

  modPropertyArr.splice(1, prefLength);

  modPropertyArr.forEach(function (item, index) {
    modProperty = modProperty + item;
    if (index > 0 && index < modPropertyArr.length - 1) {
      modProperty = modProperty + '-';
    }
  });

  return modProperty;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.helpers.stripQuotes"></a>[function <span class="apidocSignatureSpan">sass-lint.helpers.</span>stripQuotes (str)](#apidoc.element.sass-lint.helpers.stripQuotes)
- description and source-code
```javascript
stripQuotes = function (str) {
  return str.substring(1, str.length - 1);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sass-lint.ruleToggler"></a>[module sass-lint.ruleToggler](#apidoc.module.sass-lint.ruleToggler)

#### <a name="apidoc.element.sass-lint.ruleToggler.getToggledRules"></a>[function <span class="apidocSignatureSpan">sass-lint.ruleToggler.</span>getToggledRules (ast)](#apidoc.element.sass-lint.ruleToggler.getToggledRules)
- description and source-code
```javascript
getToggledRules = function (ast) {
  var toggledRules = {
    ruleEnable: {
      // Format in here is [isEnabled, line, column]
    },
    globalEnable: []
  };
  if (!ast.traverseByTypes) {
    return toggledRules;
  }
  ast.traverseByTypes(['multilineComment', 'singlelineComment'], function (comment, i, parent) {
    var content = comment.content;
    if (!content) {
      return;
    }
    var tokens = content.split(/[\s,]+/)
      .filter(function (s) {
        return s.trim().length > 0;
      });
    if (!tokens.length) {
      return;
    }
    var first = tokens[0],
        rules = tokens.slice(1);
    switch (first) {
    case 'sass-lint:disable':
      addDisable(toggledRules, rules, comment.start.line, comment.start.column);
      break;
    case 'sass-lint:enable':
      addEnable(toggledRules, rules, comment.start.line, comment.start.column);
      break;
    case 'sass-lint:disable-block':
      // future ref: not sure what the appropriate behavior is if there is no parent block; currently NPEs
      addDisableBlock(toggledRules, rules, parent);
      break;
    case 'sass-lint:disable-all':
      addDisableAll(toggledRules, comment.start.line, comment.start.column);
      break;
    case 'sass-lint:enable-all':
      addEnableAll(toggledRules, comment.start.line, comment.start.column);
      break;
    case 'sass-lint:disable-line':
      addDisableLine(toggledRules, rules, comment.start.line);
      break;
    default:
      return;
    }
  });
  // Sort these toggle stacks so reading them is easier (algorithmically).
  // Usually already sorted but since it's not guaranteed by the contract with gonzales-pe, ensuring it is.
  toggledRules.globalEnable.sort(sortRange);
  Object.keys(toggledRules.ruleEnable).map(function (ruleId) {
    toggledRules.ruleEnable[ruleId].sort(sortRange);
  });
  return toggledRules;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sass-lint.ruleToggler.isResultEnabled"></a>[function <span class="apidocSignatureSpan">sass-lint.ruleToggler.</span>isResultEnabled (toggledRules)](#apidoc.element.sass-lint.ruleToggler.isResultEnabled)
- description and source-code
```javascript
isResultEnabled = function (toggledRules) {
  return function (ruleResult) {
    var ruleId = ruleResult.ruleId;
    // Convention: if no column or line, assume rule is targetting 1.
    var line = ruleResult.line || 1;
    var column = ruleResult.column || 1;
    var isGloballyEnabled = toggledRules.globalEnable
      .reduce(function (acc, toggleRange) {
        return isBeforeOrSame(line, column, toggleRange[1], toggleRange[2])
          ? acc
          : toggleRange[0];
      }, true);
    if (!isGloballyEnabled) {
      return false;
    }
    if (!toggledRules.ruleEnable[ruleId]) {
      return true;
    }
    var isRuleEnabled = toggledRules.ruleEnable[ruleId]
      .reduce(function (acc, toggleRange) {
        return isBeforeOrSame(line, column, toggleRange[1], toggleRange[2])
          ? acc
          : toggleRange[0];
      }, true);
    if (!isRuleEnabled) {
      return false;
    }
    return true;
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sass-lint.selector_helpers"></a>[module sass-lint.selector_helpers](#apidoc.module.sass-lint.selector_helpers)

#### <a name="apidoc.element.sass-lint.selector_helpers.constructSelector"></a>[function <span class="apidocSignatureSpan">sass-lint.selector_helpers.</span>constructSelector (val)](#apidoc.element.sass-lint.selector_helpers.constructSelector)
- description and source-code
```javascript
constructSelector = function (val) {
  var content = null;

  if (val.is('arguments')) {
    content = constructSubSelector(val, '(', ')', constructSelector);
  }

  else if (val.is('atkeyword')) {
    content = constructSubSelector(val, '@', '', constructSelector);
  }

  else if (val.is('attributeSelector')) {
    content = constructSubSelector(val, '[', ']', constructSelector);
  }

  else if (val.is('class')) {
    content = addGrammar(val, '.', '');
  }

  else if (val.is('id')) {
    content = addGrammar(val, '#', '');
  }

  else if (val.is('interpolation')) {
    content = constructSubSelector(val, '#{', '}', constructSelector);
  }

  else if (val.is('nth')) {
    content = addGrammar(val, '(', ')');
  }

  else if (val.is('nthSelector')) {
    content = constructSubSelector(val, ':', '', constructSelector);
  }

  else if (val.is('parentheses')) {
    content = constructSubSelector(val, '(', ')', constructSelector);
  }

  else if (val.is('placeholder')) {
    content = constructSubSelector(val, '%', '', constructSelector);
  }

  else if (val.is('pseudoClass')) {
    content = constructSubSelector(val, ':', '', constructSelector);
  }

  else if (val.is('pseudoElement')) {
    content = addGrammar(val, '::', '');
  }

  else if (val.is('space')) {
    content = ' ';
  }

  else if (val.is('variable')) {
    content = constructSubSelector(val, '$', '', constructSelector);
  }

  else if (simpleIdents.indexOf(val.type) !== -1) {
    content = val.content;
  }

  else if (subSelectors.indexOf(val.type) !== -1) {
    content = constructSubSelector(val, '', '', constructSelector);
  }

  return content;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
