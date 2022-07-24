# @kdujs/eslint-config-prettier

> eslint-config-prettier for Kdu

This config is specifically designed to be used by `@kdujs/cli` & `create-kdu` setups
and is not meant for outside use (it can be used but some adaptations
on the user side might be needed - for details see the config file).

## Installation

In order to work around [a known limitation in ESLint](https://github.com/eslint/eslint/issues/3458), we recommend you to use this package alongside `@rushstack/eslint-patch`, so that you don't have to install too many dependencies:

```sh
npm add --dev @kdujs/eslint-config-prettier @rushstack/eslint-patch
```

Please also make sure that you have `prettier` and `eslint` installed.

## Usage

Add `"@kdujs/eslint-config-prettier"` to the `"extends"` array in your `.eslintrc.cjs` file. Make sure to put it **last**, so it gets the chance to override other configs.

```js
require("@rushstack/eslint-patch/modern-module-resolution")

module.exports = {
  extends: [
    // ... other configs
    "@kdujs/eslint-config-prettier"
  ]
}
```

## Further Reading

The default config is based on the recommended configuration of [`eslint-plugin-prettier`](https://github.com/prettier/eslint-plugin-prettier/#recommended-configuration), which also depends on [`eslint-config-prettier`](https://github.com/prettier/eslint-config-prettier). Please refer to their corresponding documentations for more implementation details.
