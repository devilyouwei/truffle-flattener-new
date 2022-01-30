# harmony-flattener

A fork of `truffle-flattener`  
- `@solidity-parser/parser` version bumped
- inline comment replacing (`//` -> `/* */`)


Reason: harmony block explorer verification fails if there is any `//` comment

[![npm](https://img.shields.io/npm/v/truffle-flattener.svg)](https://www.npmjs.com/package/harmony-flattener)

Truffle/Harmony Flattener concats solidity files from Truffle and Buidler projects 
with all of their dependencies.

This tool helps you to verify contracts developed with Truffle and Buidler 
on [Etherscan](https://etherscan.io), or debugging them on
[Remix](https://remix.ethereum.org), by merging your files and their
dependencies in the right order.

If you are still using Truffle, we recommend you try [Buidler](https://github.com/nomiclabs/buidler), 
our Ethereum development environment, which is much faster and flexible.

# Installation

`npm install harmony-flattener -g`

# Usage

Just intall it with npm in your truffle project and run
`harmony-flattener <solidity-files>`.

# Limitations

Aliased imports (eg: `import {symbol1 as alias, symbol2} from "filename";`) are
not supported by `truffle-flattener`/`harmony-flattener`.
