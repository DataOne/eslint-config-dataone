# DataOne JavaScript Linter

This Repository is the collection of the DataOne TypeScript Linter files.

## Installation

The package can be installe with the following command:
`npm i --save-dev eslint-config-dataone`

## Usage

You have to extend the ESLint File by this module. If no ESLint file is existent, create one (.eslintrc.json).

```JSON
{
    "extends": [
        "eslint-config-dataone"
    ]
}
```

There are specific configs for the different Framework. They all inherit from the default Template:

- default: `eslint-config-dataone`
- Angular: `eslint-config-dataone/angular`
- React: `eslint-config-dataone/react`

With the ESLint Plugin for VSCode, the errors and warnings are shown in the code directly.

To print all Errors and Warnings, you can type `npx eslint .` in the console.
With `npx eslint --fix .` some Errors can be automatically fixed.

Its also possible to autofix all Problems on saving. Therefore, you have to add the following code to the VSCode Settings (Preferences > Settings > JSON view):

```JSON
"editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
},
```

## Common Errors

```none
0:0  error  Parsing error: Cannot read file 'c:\*path*\tsconfig.json'
```

If this Error occures, it helps to ceate a *.vscode* folder with a *settings.json* file in the root directory. In that file, you define the relative path to the project.

```JSON
{
  "eslint.workingDirectories": [
    "src"
  ]
}
```
