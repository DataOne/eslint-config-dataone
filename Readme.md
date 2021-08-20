# DataOne JavaScript Linter

This Repository is the collection of the DataOne TypeScript Linter files.

## Installation

The package can be installe with the following command:
`npm i eslint-config-dataone`

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
