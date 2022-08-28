# Sudoo-JSON

[![Continuous Integration](https://github.com/SudoDotDog/Sudoo-Json/actions/workflows/ci.yml/badge.svg)](https://github.com/SudoDotDog/Sudoo-Json/actions/workflows/ci.yml)
[![codecov](https://codecov.io/gh/SudoDotDog/Sudoo-Json/branch/master/graph/badge.svg)](https://codecov.io/gh/SudoDotDog/Sudoo-Json)
[![npm version](https://badge.fury.io/js/%40sudoo%2Fjson.svg)](https://badge.fury.io/js/%40sudoo%2Fjson)
[![downloads](https://img.shields.io/npm/dm/@sudoo/json.svg)](https://www.npmjs.com/package/@sudoo/json)

JSON tools

## Install

```sh
yarn add @sudoo/json
# Or
npm install @sudoo/json --save
```

## Parse

```ts
import { JSONParser } from "@sudoo/json";

const parser: JSONParser = JSONParser.from(`{
    "hello": "world"
}`);

parser.parseOrThrow(); // Return Object if Valid, Throw Error if invalid
parser.parseOrDefault({
    hello: "nothing",
}); // Return Object if Valid, Default if invalid
```

## Stringify

```ts
import { JSONStringifier } from "@sudoo/json";

const stringifier: JSONStringifier = JSONStringifier.from({
    hello: "world",
});

parser.stringify(); // Stringify
parser.stringify(2); // Stringify with space
```
