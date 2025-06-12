# LEARN TYPESCRIPT

## Setup

How to initialise a TypeScript Project

- `npm init -y`
- Then install typescript as dev dependency `npm i --save-dev typescript`
- Create an initialisation config file `npx tsc --init` - creates the `tsconfig.json` file.

## Running the script.ts

`npx tsc script.ts --noEmitOnError`- compiles the script.ts file into a JavaScript file. Removes everything JavaScript doesn't understand, like types and interfaces.

- `npx tsc script.ts` - compiles the script.ts file into a JavaScript file, but does not check for errors.
- `npx tsc script.ts --watch` - compiles the script.ts file into a JavaScript file and watches for changes.
- `npx tsc script.ts --outDir dist` - compiles the script.ts file into a JavaScript file and outputs it to the dist folder.

## Setting up by using a bundler - Vite

- `npm create vite@latest` - creates a new Vite project.

After this you can remove the boilerplate files and folders that you don't need.

Here are some of the commands you can use in a Vite project:

- `npm install` - installs the dependencies.
- `npm run dev` - starts the development server.
- `npm run build` - builds the project for production.
- `npm run preview` - previews the production build.

## Understanding the tsconfig.json file

- `compilerOptions` - contains the options for the TypeScript compiler.
- `target` - specifies the ECMAScript target version. For example, `ES6`, `ES2015`, `ES2020`, etc.
- `module` - specifies the module system to use. For example, `commonjs`, `esnext`, etc.
- `forceConsistentCasingInFileNames` - ensures that the casing of file names is consistent across the project.
- `strict` - enables all strict type-checking options.
- `esModuleInterop` - enables emit interoperability between CommonJS and ES Modules via creation of namespace objects for all imports.
- `skipLibCheck` - skips type checking of declaration files.

### Relevant Resources on Configuring TypeScript/Link

- [Config Bases GitHub](https://github.com/tsconfig/bases)
- [Config Options Documentation](https://www.typescriptlang.org/tsconfig)
