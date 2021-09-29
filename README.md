<img src="https://cdn.edge.network/assets/img/edge-logo-green.svg" width="200">

# TypeScript ESLint Config

ESLint config for Edge TypeScript projects.

## Usage

Install to your project:

```bash
npm i --save-dev @edge/eslint-config-typescript
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

## Quirks and Solutions

### Very long lines

Occasionally, the following combination of rules can conflict:

- [nonblock-statement-body-position](https://eslint.org/docs/rules/nonblock-statement-body-position) requires all single-statement conditionals to be on a single line
- [curly](https://eslint.org/docs/rules/curly) prevents single-statement conditionals from using braces
- [max-len](https://eslint.org/docs/rules/max-len) enforces a maximum line length of 120 characters

This is most common when you have a particularly long line of code that can't be cleanly broken over, such as a log message. There are a few possible solutions to this:

- Shorten the line, e.g. by assigning variables to break it apart (which may have the side effect of then requiring `curly` anyway)
- If the length is due to a string, you could break it up into an array of strings and `.join('')` at the end
- Place the statement on a single line to meet the constraints of `nonblock-...` and `curly` rules, then add `// eslint-disable-next-line max-len` above it to break the tie. (Other rules can be disabled in a similar way, but this is the 'cleanest' one to disable with the least divergence from convention)
