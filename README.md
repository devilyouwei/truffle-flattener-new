# truffle-flattener-new

A fork of `truffle-flattener`, `harmony-flattener`

-   `@solidity-parser/parser` version bumped
-   inline comment replacing (`//` -> `/* */`)
-   fix `http://` become `http:/*....`

Truffle Flattener concats solidity files from Truffle and Buidler projects with all of their dependencies.

Flattener your solidity code can:

-   help you verify your contract on bscscan and ethscan...
-   use `solcjs` to compile your code

# Installation

```bash
yarn add truffle-flattener-new
#or
npm install --save truffle-flattener-new
```

# Usage

1. use `package.json` scripts, terminal cmd

```
truffle-flattener <solidity-files>
```

2. import in other js file

```js
const flat = require('truffle-flattener-new')
const res = await flat([filename])
fs.writeFileSync(filename, res)
```

# Limitations

Aliased imports (eg: `import {symbol1 as alias, symbol2} from "filename";`) are not supported by
`truffle-flattener`/`harmony-flattener`.
