# Cucumber.js TypeScript Path Alias Issue

When using TypeScript path aliases (configured in `tsconfig.json`), Cucumber.js does not correctly resolve these paths, resulting in module resolution errors during runtime.

### Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/samydoesit/cucumber-typescript-path-alias-reproduction.git
cd cucumber-typescript-path-alias-reproduction
npm install

# Run the tests
npm run test
```

### Issue

```bash
Error: Cannot find package '@/index.js' imported from /cucumber-typescript-path-alias-reproduction/features/step_definitions/steps.ts
    at packageResolve (/cucumber-typescript-path-alias-reproduction/node_modules/ts-node/dist-raw/node-internal-modules-esm-resolve.js:757:9)
    at moduleResolve (/cucumber-typescript-path-alias-reproduction/node_modules/ts-node/dist-raw/node-internal-modules-esm-resolve.js:798:18)
    at Object.defaultResolve (/cucumber-typescript-path-alias-reproduction/node_modules/ts-node/dist-raw/node-internal-modules-esm-resolve.js:912:11)
    at /cucumber-typescript-path-alias-reproduction/node_modules/ts-node/src/esm.ts:218:35
    at entrypointFallback (/cucumber-typescript-path-alias-reproduction/node_modules/ts-node/src/esm.ts:168:34)
    at /cucumber-typescript-path-alias-reproduction/node_modules/ts-node/src/esm.ts:217:14
    at addShortCircuitFlag (/cucumber-typescript-path-alias-reproduction/node_modules/ts-node/src/esm.ts:409:21)
    at resolve (/cucumber-typescript-path-alias-reproduction/node_modules/ts-node/src/esm.ts:197:12)
    at nextResolve (node:internal/modules/esm/hooks:865:28)
    at Hooks.resolve (node:internal/modules/esm/hooks:303:30)
```
