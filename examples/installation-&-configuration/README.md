* goal
  * karma-jasmine-html-reporter installation

# How has it been created?
* `npm init -y`
* `npm install karma karma-jasmine-html-reporter --save-dev`
* `./node_modules/karma/bin/karma init` & prompt selecting ALL default
* adjust | "karma.conf.js" 

# how to run?
* `./node_modules/karma/bin/karma start`
  * Problems:
    * Problem1: "Cannot load browser "Chrome": it is not registered! Perhaps you are missing some plugin?"
      * Solution: add Karma.conf.js plugins `require('karma-chrome-launcher'),`
    * Problem2: Nothing is displayed as no test was found
      * 💡Solution: `client.clearContext: false`💡
