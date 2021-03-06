# How to get started with a Jest boilerplate

## Install [Node Version Manager](https://github.com/nvm-sh/nvm)
``` bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | zsh
```

## Install Node.js via nvm
``` bash
nvm install node
```

## [Create a Node.js module](https://docs.npmjs.com/creating-node-js-modules)
``` bash
npm init -y
```

## Install and set up ESLint

### Install ESLint

``` bash
npm i -D eslint

npx eslint --init
```

### Set up Eslint

``` javascript
// .eslintrc.js

export default {
  env: {
    browser: true,
    es2021: true,
    jest: true,
  },
  extends: [
    'airbnb-base',
  ],
  globals: {
    context: true,
  },
  parserOptions: {
    ecmaVersion: 12,
    sourceType: 'module',
  },
  rules: {
    indent: ['error', 2],
    'no-trailing-spaces': 'error',
    curly: 'error',
    'brace-style': 'error',
    'no-multi-spaces': 'error',
    'space-infix-ops': 'error',
    'space-unary-ops': 'error',
    'no-whitespace-before-property': 'error',
    'func-call-spacing': 'error',
    'space-before-blocks': 'error',
    'keyword-spacing': ['error', { before: true, after: true }],
    'comma-spacing': ['error', { before: false, after: true }],
    'comma-style': ['error', 'last'],
    'comma-dangle': ['error', 'always-multiline'],
    'space-in-parens': ['error', 'never'],
    'block-spacing': 'error',
    'array-bracket-spacing': ['error', 'never'],
    'object-curly-spacing': ['error', 'always'],
    'key-spacing': ['error', { mode: 'strict' }],
    'arrow-spacing': ['error', { before: true, after: true }],
    'react/prop-types': 'off',
    'react/jsx-uses-react': 'off',
    'react/react-in-jsx-scope': 'off',
    'jsx-a11y/label-has-associated-control': ['error', { assert: 'either' }],
    'no-unused-vars': ['error', { varsIgnorePattern: 'jsx' }],
  },
};

```

## Install and set up Jest

### Install Jest

``` bash
npm i -D jest @types/jest jest-plugin-context
```

### Set up Jest

``` javascript
// jest.config.js

module.exports = {
  setupFilesAfterEnv: [
    'jest-plugin-context/setup',
  ],
  modulePathIgnorePatterns: [
    '<rootDir>/.cache',
  ],
};

```

## Initialize and set up Git

### Initialize Git

``` bash
git init
```

### Set up Git

``` gitignore
# .gitignore

node_modules

```

