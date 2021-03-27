# @ngx-playwright

Utilities for using playwright to test angular applications.

This repository contains multiple packages in the `packages/` folder. Every package has its own README detailing what it does and how to use it.

## Development

This repository is set up using [yarn 2](https://yarnpkg.com) and [snuggery](https://github.com/snuggery/snuggery).

To install dependencies, run the following comment in the folder of the package, or run in the repository root folder to build all packages:

```bash
yarn
```

To build a package, run

```bash
yarn build
# or
yarn sn build
# or, if you have @snuggery/global installed globally
sn build
```

The package will be built in `<package folder>/dist`, e.g. `packages/jest/dist`. You can test your build by refering to that folder in a package.json, e.g.

```json
// in dependencies, or via resolutions
{
  "@ngx-playwright/jest": "file:///path/to/ngx-playwright/packages/jest/dist"
}
```

Before opening a pull request, mark the packages that need to be released afterwards using

```bash
yarn version check --interactive
```

To publish, run

```bash
yarn sn deploy
# or, if @snuggery/global is installed globally
sn deploy
```

## License

See [LICENSE.md](./LICENSE.md)
