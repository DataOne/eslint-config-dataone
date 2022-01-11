# DataOne JavaScript Linter

This Repository is the collection of the DataOne TypeScript Linter files.

## Installation

The package can be installed with the following command:
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

## Usage with Prettier
You can use ESLint in combination with the Prettier-autoformatter. To do so, following steps have to be followed.  
You have to install the VSCode Extensions [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) and [Prettier ESLint](https://marketplace.visualstudio.com/items?itemName=rvest.vs-code-prettier-eslint). The *Prettier ESLint* Extension lets you format a File with both Prettier and ESLint.  
For better usage, some configs have to adjusted. These can be found in the auxiliaryConfigs folder:
- *.vscode/settings.json*  
- *.editorconfig*
- *prettierrc.json*

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
