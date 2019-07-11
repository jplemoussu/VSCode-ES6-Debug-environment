# VSCode + Node.js + ES6 + debugger environment

Environment for Visual Studio Code as per [Dustin Callaway: Debugging ES6 in visual studio code](https://medium.com/@drcallaway/debugging-es6-in-visual-studio-code-4444db797954) with additional mods:
* Replaced `babel-preset-es2015` (deprecated) with `babel-preset-env`. [See Babel docs](https://babeljs.io/docs/en/env/)
* Added build task `compile` in `tasks.json`.
* Added prelaunch config in `package.json`:  `"preLaunchTask": "compile"`. This automatically transpiles the ES6 code before launching the debugger.

Steps to use
1. `Git clone https://github.com/jplemoussu/VSCode-ES6-Debug-environment.git <projectname>`
2. `yarn install` to install node modules
3. Open any .js file in the `/src` folder with VSCode and debug by running `ES6 Debugger` from the debugger menu.

`package.json` includes following npm dependencies:
* babel-cli
* babel-plugin-transform-runtime
* babel-preset-env
