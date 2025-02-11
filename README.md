# karma-jasmine-html-reporter

[![npm version](https://img.shields.io/npm/v/karma-jasmine-html-reporter.svg)](https://www.npmjs.com/package/karma-jasmine-html-reporter) [![npm downloads](https://img.shields.io/npm/dm/karma-jasmine-html-reporter.svg)](https://www.npmjs.com/package/karma-jasmine-html-reporter)

* == reporter /
  * dynamically shows tests results | "debug.html"

![alt tag](/screenshots/reporter_1.png)

## Installation

```bash
npm install karma-jasmine-html-reporter --save-dev
```

## Configuration
```js, , tittle=karma.conf.js
module.exports = function(config) {
  config.set({
    frameworks: ['jasmine'],
    plugins: [
        require('karma-jasmine'),
        require('karma-jasmine-html-reporter')
    ],
    client: {
        jasmine: {
            // you can add configuration options for Jasmine here
            // the possible options are listed at https://jasmine.github.io/api/edge/Configuration.html
            // for example, you can disable the random execution with `random: false`
            // or set a specific seed with `seed: 4321`
        }
    },
    reporters: ['kjhtml']
  });
};
```
#### `jasmineHtmlReporter`  
* allows
  * configuring options

* _Example:_
```js, tittle=karma.conf.js
module.exports = function(config) {
  config.set({

    // MULTIPLE reporters
    reporters: ['kjhtml', 'mocha'],   //  + 'karma-mocha-reporter' plugin

    // configure options
    jasmineHtmlReporter: {
      suppressAll: true,    // Suppress ALL messages (overrides other suppress settings)
      suppressFailed: true  // Suppress failed messages
    }

  });
};
```

## How to run?

```bash
karma start --reporters reporter1, reporter2, ...
```

* _Example:_
  ```bash
  karma start --reporters kjhtml
  ```

## Version compatibility

jasmine Version | karma-jasmine-html-reporter version
-|-
2.x | 0.2.2
3.x | 1.x
4.x | 2.x
