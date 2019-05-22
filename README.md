<div align="center">
  <img src="https://res.cloudinary.com/adonisjs/image/upload/q_100/v1557762307/poppinss_iftxlt.jpg" width="600px">
</div>

# Adonis application
[![circleci-image]][circleci-url] [![npm-image]][npm-url] ![](https://img.shields.io/badge/Typescript-294E80.svg?style=for-the-badge&logo=typescript)

The application class for AdonisJs to know more about the environment and project structure of your AdonisJs applications.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## Table of contents

- [Usage](#usage)
- [rcParser](#rcparser)
- [API Docs](#api-docs)
- [Change log](#change-log)
- [Contributing](#contributing)
- [Authors & License](#authors--license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Usage
Ideally you shouldn't be installing this module directly, hence it is part of AdonisJs by default. However, installing module directly is helpful when testing AdonisJs specific addons.

```sh
npm i @poppinss/application

# Yarn
yarn add @poppinss/application
```

and then use it as follows:

```ts
import { Application } from '@poppinss/application'
import { Ioc } from '@adonisjs/fold'

const app = new Application(
  '1.0.0',
  __dirname,
  new Ioc(),
  require('./adonisrc.json'),
)
```

The constructor takes 4 arguments, which you fake during testings.

| Argument position | Description |
|------------------|------------------|
| `0 (version)` | The version of `@adonisjs/core` package |
| `1 (appRoot)` | The application root |
| `3 (ioc)` | Instance of IoC container |
| `4 (rcContents)` | Contents of `.adonisrc.json` file. You can also provide an empty object |

## rcParser
The application instance will parse the contents of `.adonisrc.json` file. However, if you need the parser, you can access and use it as follows.

```ts
import { rcParser } from '@poppinss/application'
rcParser.parse(require('.adonisrc.json'))
```

## API Docs
Following are the autogenerated files via Typedoc

* [API](docs/README.md)

## Change log

The change log can be found in the [CHANGELOG.md](CHANGELOG.md) file.

## Contributing

Everyone is welcome to contribute. Please go through the following guides, before getting started.

1. [Contributing](https://adonisjs.com/contributing)
2. [Code of conduct](https://adonisjs.com/code-of-conduct)


## Authors & License
[Harminder virk](https://github.com/Harminder virk) and [contributors](https://github.com/poppinss/application/graphs/contributors).

MIT License, see the included [MIT](LICENSE.md) file.

[circleci-image]: https://img.shields.io/circleci/project/github/poppinss/application/master.svg?style=for-the-badge&logo=circleci
[circleci-url]: https://circleci.com/gh/poppinss/application "circleci"

[npm-image]: https://img.shields.io/npm/v/@poppinss/application.svg?style=for-the-badge&logo=npm
[npm-url]: https://npmjs.org/package/@poppinss/application "npm"
