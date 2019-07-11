# VSCode + Node.js + ES6 + debugger environment

Environment for Visual Studio Code as per [Dustin Callaway: Debugging ES6 in visual studio code](https://medium.com/@drcallaway/debugging-es6-in-visual-studio-code-4444db797954) with additional mod:
* Added build task `compile` in `tasks.json`. This allows to use the shortcut `Shift+CMD+B` to transpile the code

# Steps to use
1. `Git clone https://github.com/jplemoussu/VSCode-ES6-Debug-environment.git <projectname>`
2. `yarn install` to install node modules
3. SHIFT+CMD+B to transpile code
4. Open any .js file in the `/src` folder with VSCode and debug by running `ES6 Debugger` from the debugger menu.

`package.json` includes following npm dependencies:
* babel-cli
* babel-preset-es2015

# About debuging transpiled code

When you set a breakpoint, the debug adapter has to figure out the path to the transpiled version, which is what is running in Node. The debug adapter uses the `outFiles` attribute in the `launch.json` to find all the transpiled .js files, and parses them for a source map, which contains the locations of its associated original .js files.

When you build with source maps enabled, it produces an *.js.map file. The debug adapter searches for the full path to find the source map file to use. If there is no match, then it can't bind the breakpoint, and it will turn gray.
