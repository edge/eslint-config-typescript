<img src="https://cdn.edge.network/assets/img/edge-logo-green.svg" width="200">

# TypeScript ESLint Config

ESLint config for Edge TypeScript projects.

## Usage

Install to your npm project using a [GitHub dependency](https://docs.npmjs.com/cli/v6/configuring-npm/package-json#github-urls):

```bash
npm i --save-dev edge/eslint-config-typescript#v1
```

This package specifies peer dependencies, which [you may need to add manually to your project](https://nodejs.org/en/blog/npm/peer-dependencies/). To do so, run the following in shell at your npm project root:

```bash
npm i --save-dev \
  @typescript-eslint/eslint-plugin \
  @typescript-eslint/parser \
  eslint \
  typescript
```

Afterwards, add the following configuration to your ESLint configuration:

```json
{
  "parser": "@typescript-eslint/parser",
  "plugins": [
    "@typescript-eslint"
  ],
  "extends": [
    "@edge/eslint-config-typescript"
  ]
}
```

Finally, configure your npm scripts, IDE, etc. as your project requires.
