<img src="https://cdn.edge.network/assets/img/edge-logo-green.svg" width="200">

# TypeScript ESLint Config

ESLint config for Edge TypeScript projects.

For JavaScript config without TypeScript-specific rules, see [edge/eslint-config-javascript](https://github.com/edge/eslint-config-javascript)

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

## License

Edge is the infrastructure of Web3. A peer-to-peer network and blockchain providing high performance decentralised web services, powered by the spare capacity all around us.

Copyright notice
(C) 2022 Edge Network Technologies Limited <support@edge.network><br />
All rights reserved

This product is part of Edge.
Edge is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version ("the GPL").

**If you wish to use Edge outside the scope of the GPL, please contact us at licensing@edge.network for details of alternative license arrangements.**

**This product may be distributed alongside other components available under different licenses (which may not be GPL). See those components themselves, or the documentation accompanying them, to determine what licenses are applicable.**

Edge is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

The GNU General Public License (GPL) is available at: https://www.gnu.org/licenses/gpl-3.0.en.html<br />
A copy can be found in the file GPL.md distributed with
these files.

This copyright notice MUST APPEAR in all copies of the product!
