# Remove Junks Plugin

[![npm (scoped)](https://img.shields.io/npm/v/@glitchapp/remove-junks-plugin.svg?style=flat-square)]()
[![Travis](https://img.shields.io/travis/glitchapp/glitch.svg?style=flat-square)]()
[![npm](https://img.shields.io/npm/l/@glitchapp/remove-junks-plugin.svg?style=flat-square)]()

> This package is part of [Glitch](https://github.com/glitchapp) project

A webpack plugin to remove junk chunk's files

## Installation

```sh
$ npm install @glitchapp/remove-junks-plugin
```

## Usage

```javascript
// webpack.config.js
const { RemoveJunksPlugin } = require('@glitchapp/remove-junks-plugin')

module.exports = {
  entry: {
    app: './app.js'
  },
  ...
  output: {
    filename: 'bundle.js'
  },
  ...
  plugins: [
    // This removes 'bundle.js'
    // NOTE: It works even if a chunk has multiple output files (i.e. if you use a plugin like extract-text-webpack-plugin)
    new RemoveJunksPlugin(['app'])
  ]
}
```

## Options

```javascript
new RemoveJunksPlugin(chunks)
```

| Name                | Type       | Description                                   |
| :-----------------: | :--------: | :-------------------------------------------: |
| `chunks` (required) | `string[]` | A lists of all chunk names you want to remove |

## Contributing

We value and appreciate your help, please read [CONTRIBUTING.md](../../CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Running the tests

```sh
$ npm test
```

## Acknowledgments

Inspired by the awesome work of Alex Lu in their [suppress-chunks-webpack-plugin](https://github.com/alxlu/suppress-chunks-webpack-plugin) webpack plugin.

## License

This project is licensed under the [MIT License](./LICENSE) terms
