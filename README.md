# VSCode + Node.js + ES6 + debugger environment

Environment for Visual Studio Code as per [Dustin Callaway: Debugging ES6 in visual studio code](https://medium.com/@drcallaway/debugging-es6-in-visual-studio-code-4444db797954)

Before launching debugger run `npm run compile` from terminal to transpile code from ES6 to ES5.

`package.json` includes following npm dependencies:
* babel-cli
* babel-preset-es2015
* bluebird
* cheerio
* colors
* debug
* dotenv
* lodash
* promise-retry
* request
* request-promise