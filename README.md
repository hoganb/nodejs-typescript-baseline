# nodejs-typescript-baseline

Node.js TypeScript baseline reference project setup

# Scripts

- `npm ci`: Clean install
- `npm run clean`: Clean project
- `npm run build`: Compile, bundle and minify project
- `npm run lint`: Code quality check
- `npm run lint:fix`: Code quality fixes
- `npm test`: Run unit tests
- `npm run test:mutation`: Run mutation tests

# Features

- **Node.js**: Runtime `"node": "^16.0.0"` and `"npm": "^8.5.1"`
- **TypeScript**: Code type checked and transpiled to JavaScript `"^4.9.3"`
- **Esbuild**: Code bundled and minified with source maps for debugging
- **Linting**: Code quality using `eslint`, `prettier` and `cspell`
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
├── jest.config.js      # Jest config file
├── package.json        # Package json file
├── stryker.conf.json   # Stryker config file
└── tsconfig.json       # Typescript compiler configuration
```
