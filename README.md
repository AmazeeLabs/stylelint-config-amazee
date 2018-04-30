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

## [Changelog](CHANGELOG.md)

## [License](LICENSE)
