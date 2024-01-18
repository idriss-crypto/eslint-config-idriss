# eslint-config-idriss

Eslint config to apply linting rules set by [IDriss](https://idriss.xyz)

## Usage

npm:

```bash
# npm
npm install --save-dev eslint-config-idriss

# yarn
yarn add -D eslint eslint-config-idriss @typescript-eslint/eslint-plugin@latest @typescript-eslint/parser

# pnpm
pnpm add -D eslint eslint-config-idriss @typescript-eslint/eslint-plugin@latest @typescript-eslint/parser
```

Run this command to install required peer depenedencies:

```bash
npx install-peerdeps --dev eslint-config-airbnb
```

Extend this configuration in your eslint config:

```js
module.exports = {
    extends: 'eslint-config-idriss',
};
```

We highly recommend to create prettier config file so eslint can also use rules from prettier to enforce code formatting:

Example `eslint-config.cjs`:

```js
/** @type {import("prettier").Config} */
export default {
    singleQuote: true,
    trailingComma: 'all',
    useTabs: false,
    endOfLine: 'lf',
    semi: true,
    tabWidth: 4,
    printWidth: 80,
    arrowParens: 'always',
    editorconfig: true,
};
```

We also recommend to use editor config file to apply formatting rules:

Example `.editorconfig` file:

```
root = true

[*]
end_of_line = lf
charset = utf-8
indent_size = 2
indent_style = space
trim_trailing_whitespace = true
insert_final_newline = true
```
