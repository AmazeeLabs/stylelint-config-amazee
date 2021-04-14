# stylelint-config-amazee

Based on [`stylelint-config-standard`](https://github.com/stylelint/stylelint-config-standard).

To see the rules that this config uses, please read the [config itself](./index.js).

## Installation

```bash
npm install stylelint-config-amazee --save-dev
#OR
yarn add stylelint-config-amazee --dev

```

## Usage

If you've installed `stylelint-config-amazee` locally within your project, just set your project root `.stylelint` file config to:

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

## IDE Extensions
* VSCODE
    Name: stylelint-plus
    Id: hex-ci.stylelint-plus
    Description: Modern CSS/SCSS/Less linter for vscode, *support auto fix on save*.
    Publisher: Hex
    VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=hex-ci.stylelint-plus
** Read the Extension's help text to show you how to update your user settings. E.g. Setting which code languages you'd like Stylelint to work with and whether to auto format on save etc.
** My VsCode settings - with Global Stylelint:

```json
    "stylelint.enable": true,
    "css.validate": false,
    "less.validate": false,
    "scss.validate": false,
    "[scss]": {
      "editor.defaultFormatter": "hex-ci.stylelint-plus",
      "editor.formatOnSave": true,
      "editor.formatOnPaste": false
    },
    "stylelint.configOverrides": {
      "extends": "/Users/username/git/stylelint-config-amazee/index.js",
      "rules": {
        "at-rule-no-unknown": [
          true,
          {
            "ignoreAtRules": [
              "extend",
              "ignores",
              "include",
              "media",
              "if",
              "else",
              "mixin",
              "for",
              "each"
            ]
          }
      ]
    }
  },
```

* PHPSTORM
    https://www.jetbrains.com/help/phpstorm/using-stylelint-code-quality-tool.html

* Other IDEs: https://stylelint.io/user-guide/integrations/editor
    
* General info: https://stylelint.io/

## Updates
* Make your changes.
* Update [Changelog](CHANGELOG.md).
* Commit your changes.
* Update [package](https://docs.npmjs.com/getting-started/publishing-npm-packages#how-to-update-a-package).

## [Changelog](CHANGELOG.md)

## [License](LICENSE)
