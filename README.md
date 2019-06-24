# VSCode + Node.js + ES6 + debugger environment

Environment for Visual Studio Code as per [Dustin Callaway: Debugging ES6 in visual studio code](https://medium.com/@drcallaway/debugging-es6-in-visual-studio-code-4444db797954)

Steps to use
1. `Git clone https://github.com/jplemoussu/VSCode-ES6-Debug-environment.git <projectname>`
2. `yarn install` to install node modules
3. `yarn compile` to transpile code from ES6 to ES5.
4. Open any .js file in the `/src` folder with VSCode and debug by running `Launch Current File` from the debugger menu.

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
