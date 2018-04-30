# stylelint-config-amazee

Based on [`stylelint-config-standard`](https://github.com/stylelint/stylelint-config-standard).

To see the rules that this config uses, please read the [config itself](./index.js).

## Installation

```bash
npm install stylelint-config-amazee --save-dev
```

## Usage

If you've installed `stylelint-config-amazee` locally within your project, just set your `stylelint` config to:

```json
{
  "extends": "stylelint-config-amazee"
}
```

If you've globally installed `stylelint-config-amazee` using the `-g` flag, then you'll need to use the absolute path to `stylelint-config-amazee` in your config e.g.

```json
{
  "extends": "/absolute/path/to/stylelint-config-amazee"
}
```

### Extending the config

Simply add a `"rules"` key to your config, then add your overrides and additions there.

For example, to change the `at-rule-no-unknown` rule to use its `ignoreAtRules` option, change the `indentation` to tabs, turn off the `number-leading-zero` rule, and add the `unit-whitelist` rule:

```json
{
  "extends": "stylelint-config-amazee",
  "rules": {
    "at-rule-no-unknown": [ true, {
      "ignoreAtRules": [
        "extends",
        "ignores"
      ]
    }],
    "indentation": "tab",
    "number-leading-zero": null,
    "unit-whitelist": ["em", "rem", "s"]
  }
}
```

### Plugins
Plugins are rules or sets of rules built by the community that support methodologies, toolsets, non-standard CSS features, or very specific use cases. See [documentation](https://stylelint.io/user-guide/configuration/#plugins) for more information.

- Disallow features that are unsupported by the browsers that you are targeting:
  - [`stylelint-no-unsupported-browser-features`](https://www.npmjs.com/package/stylelint-no-unsupported-browser-features)
- A collection of order related linting rules for stylelint:
  - [`stylelint-order`](https://www.npmjs.com/package/stylelint-order)
- [All stylelint plugins](https://www.npmjs.com/search?q=keywords:stylelint-plugin)

## Updates
* Make your changes.
* Update [Changelog](CHANGELOG.md).
* Commit your changes.
* Update [package](https://docs.npmjs.com/getting-started/publishing-npm-packages#how-to-update-a-package).

## [Changelog](CHANGELOG.md)

## [License](LICENSE)
