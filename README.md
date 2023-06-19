# nodejs-typescript-baseline

<p align="center">
  <a href="https://nodejs.org/dist/latest-v18.x/docs/api/"><img alt="Node.js version" src="https://img.shields.io/badge/node.js-v18.x.x-green"></a>
  <a href="https://docs.npmjs.com/cli/v9"><img alt="npm version" src="https://img.shields.io/badge/npm-v9.x.x-red"></a>
  <a href=""><img alt="TypeScript version" src="https://img.shields.io/badge/TypeScript-v5.x.x-blue"></a>
  <a href=""><img alt="CI/CD GitHub Actions" src="https://img.shields.io/badge/CI/CD-GitHub_Actions-4b83f3"></a>
</p>

<p align="center">
  <a href="https://github.com/prettier/prettier"><img alt="code format: prettier" src="https://img.shields.io/badge/code_format-prettier-ff69b4"></a>
  <a href="https://github.com/eslint/eslint"><img alt="code quality: eslint" src="https://img.shields.io/badge/code_quality-eslint-9a19e0"></a>
  <a href="https://github.com/Microsoft/TypeScript"><img alt="type check: tsc" src="https://img.shields.io/badge/type_check-tsc-blue"></a>
  <a href="https://github.com/evanw/esbuild"><img alt="build: esbuild" src="https://img.shields.io/badge/build-esbuild-f5d135"></a>
  <a href="https://github.com/jestjs/jest"><img alt="test: jest" src="https://img.shields.io/badge/test-jest-8c474f"></a>
  <a href="https://github.com/stryker-mutator/stryker-js"><img alt="test: jest" src="https://img.shields.io/badge/mutation-stryker-d15b3f"></a>
</p>

<p align="center">
  <a href="https://github.com/hoganb/nodejs-typescript-baseline/actions/workflows/ci.yml"><img alt="ci" src="https://github.com/hoganb/nodejs-typescript-baseline/actions/workflows/ci.yml/badge.svg"></a>
</p>

Node.js TypeScript baseline reference project setup

# Scripts

- `npm ci`: Clean install
- `npm run clean`: Full clean ready for `npm ci`
- `npm run format`: Code format and spell check
- `npm run format:fix`: Code format and spell check fixes
- `npm run lint`: Code quality checks
- `npm run lint:fix`: Code quality fixes
- `npm run build`: Type check, compile, bundle and minify
- `npm test`: Run unit tests
- `npm run test:mutation`: Run mutation tests
- `npm run test:unit:watch`: Run unit tests in watch mode
- `npm run updates:check`: Check dependency updates grouped by major.minor.patch
- `npm run updates:upgrade`: Upgrades dependencies grouped by major.minor.patch

**NOTE**: For `npm run updates:*` commands; can control the versions by passing `-- --target <patch|minor|major>` flag, for example:

- To only check/upgrade `minor` versions then use `npm run updates:check -- --target minor`

# Features

- **Node.js**: Runtime `"node": "^18.0.0"` and `"npm": "^9.5.0"`
- **Formatting**: Code format rules checked and fixed using `prettier` and spell checked with `cspell`
- **Linting**: Code quality rules checked and fixed using `eslint`
- **TypeScript**: Code type checked and transpiled to JavaScript using `tsc`
- **Esbuild**: Code transpiled to JavaScript, bundled and minified with source maps for debugging using `esbuild`
- **Dependency updates**: Check and upgrade achieved using `npm-check-updates`
- **Jest**: Test runner solution using `@swc/jest` transformer
- **Stryker**: Mutation tests test unit tests against the code
- **GitHub Actions**: CI pipeline integration to `build`, `lint` and `test` code
- **Miscellaneous**
  - **tslib**: Runtime library for TypeScript helpers that produces more optimized code when coupled with importHelpers tsconfig option

# Project Structure

```
.
├── src
│   └── index.ts        # Source code
├── test
│   └── index.ts        # Unit test code
│
│── ...
├── .cspell.json        # CSpell config file
├── .editorconfig       # Editor config file
├── .eslintrc.json      # Eslint config file
├── .prettierrc.json    # Prettier config file
├── jest.config.js      # Jest config file
├── package.json        # Package json file
├── stryker.conf.json   # Stryker config file
└── tsconfig.json       # Typescript compiler configuration
```
