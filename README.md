# Setup TypeScript

## Story

TypeScript is a language for application-scale JavaScript. TypeScript adds optional types to JavaScript that support tools for large-scale JavaScript applications for any browser, for any host, on any OS. TypeScript compiles to readable, standards-based JavaScript. 

## What are you going to learn?

- Installing TypeScript
- Setting up VsCode extensions
- Compile .ts files into .js

## Tasks

1. Make sure that TypeScript at least  version 4.2.0 is installed on your system.
    - Run `npm install -g typescript` globally to install TypeScript on your system.
    - Executing the `tsc -version` command in the shell shows a version number greater than 12.0.0

2. Make sure that Visual Studio Code and the required extensions are installed and set up on your system.
    - `JavaScript (ES6) code snippets` is set up in VsCode
    - `TSLint` from Microsoft is set up in VsCode. Configure settings.json file according to the extension documentation.
    - `Debugger for Chrome` is set up in VsCode
    - `Prettier` is set up in VsCode
    - `Code Metrics` which calculates complexity in TypeScript code is set up in VsCode

3. Create project repository and write your first code in TypeScript. Remember to compile it by `tsc` command.
    - Run `npm i` to install dependencies from package.json.
    - In `app.ts` write just sample `console.log('Hi there!')` line, compile code, and check what will be included in generated app.js file.
    - In the same .ts file, add asynchronous function e.g. `async function foo(): Promise<void>{}`. Compile the code with `tsc app.ts` and check how the JavaScript file will look like.
    - Do the same as in the above step, but now compile .ts file with `tsc app.ts --target ES2015`. Compare `app.ts` with `app.js` file.
    - Do the same as in the above step, but now compile .ts file with `tsc app.ts --target ESNext`. Compare `app.ts` with `app.js` file.
    - Change the output for compiled javascript files with `tsc app.ts --target ESNext --outDir ./dist`. Also remember to update script src in index.html by referencing to `dist` directory.

4. Create tsconfig.json file which specifies the root files and the compiler options required to compile the project.
    - Generate TypeScript configuration file with `tsc --init`.
    - Focus on following compiler options: `target`, `module`, `strict`, `outDir`.

5. Run the compiler in watch mode. Watch input files and trigger recompilation on changes.
    - Run `tsc app.ts --watch` command, and write sample code in a watch mode. The changes will compile automatically.

## General requirements

None

## Hints
