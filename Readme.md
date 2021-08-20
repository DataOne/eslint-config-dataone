# DataOne JavaScript Linter

This Repository is the collection of the DataOne TypeScript Linter files.

## Installation

The package can be installe with the following command:
`npm i eslint-config-dataone`

Because of ESLint limitations, some dependencies have to be installed manually. These depend on the chosen Framework.

### Angular

```Bash
npm install eslint-plugin-import@^2.22.0 @typescript-eslint/eslint-plugin@^4.4.1 @angular-eslint/eslint-plugin-template @angular-eslint/template-parser @angular/compiler @angular-eslint/eslint-plugin eslint --save-dev 
```

### React

When the typescript template was chosen during the initiation process, no dependencies have to be reinstalled. Otherwise:

```Bash
npm install eslint-plugin-import@^2.22.0 
    eslint-plugin-jsx-a11y@^6.3.1 
    eslint-plugin-react@^7.20.3 
    eslint-plugin-react-hooks@^4.0.8 
    @typescript-eslint/eslint-plugin@^4.4.1 
    --save-dev
```

### Node/no framework

```Bash
npm install eslint eslint-plugin-import
    --save-dev
```

## Usage

You have to extend the ESLint File by this module.

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
