# electron-ts-react

## A Boilerplate for an Easy Start with TypeScript, React, and Electron

[![React](docs/img/react.png)](https://reactjs.org/)
[![Webpack](docs/img/webpack.png)](https://webpack.js.org/)
[![TypeScript](docs/img/ts.png)](https://www.typescriptlang.org/)
[![Electron](docs/img/electron.png)](https://electronjs.org/)
[![Redux](docs/img/redux.png)](https://redux.js.org/)
[![Jest](docs/img/jest.png)](https://facebook.github.io/jest/)

[Electron](https://electronjs.org/) application boilerplate based on [React](https://reactjs.org/), [Redux](https://redux.js.org/), and [Webpack](https://webpack.js.org/) for rapid application development using [TypeScript](https://www.typescriptlang.org/).

## Install

Clone the repository with Git:

```bash
git clone --depth=1 git@github.com:fanjianquan/electron-ts-react.git <your-project-name>
```

And then install the dependencies:

```bash
cd <your-project-name>
npm install
```

## Usage

Both processes have to be started **simultaneously** in different console tabs:

```bash
npm run start-renderer-dev
npm run start-main-dev
```

This will start the application with hot-reload so you can instantly start developing your application.

You can also run do the following to start both in a single process:

```bash
npm run start-dev
```

## Test

Run Jest cases

```bash
npm test
```

Run e2e tests

```bash
npm run test:e2e
```

If you meet error:

```bash
Error: ChromeDriver did not start within 5000ms
```

You may set global proxy. And you have to ignore proxy for localhost.

```bash
export {no_proxy,NO_PROXY}=127.0.0.1
```

## Packaging

We use [Electron builder](https://www.electron.build/) to build and package the application. By default you can run the following to package for your current platform:

```bash
npm run dist
```

This will create a installer for your platform in the `releases` folder.

You can make builds for specific platforms (or multiple platforms) by using the options found [here](https://www.electron.build/cli). E.g. building for all platforms (Windows, Mac, Linux):

```bash
npm run dist -- -mwl

// Windows
npm run dist -- -win
// Mac
npm run dist -- -mac
// Linux
npm run dist -- -linux
```

## Husky and Prettier

This project comes with both Husky and Prettier setup to ensure a consistent code style.

To change the code style, you can change the configuration in `.prettierrc`.

In case you want to get rid of this, you can removing the following from `package.json`:

1. Remove `precommit` from the `scripts` section
1. Remove the `lint-staged` section
1. Remove `lint-staged`, `prettier`, `tslint-config-prettier`, and `husky` from the `devDependencies`

Also remove `tslint-config-prettier` from the `extends` section in `tslint.json`.

## About this project

It's forked from project [electron-typescript-react](https://github.com/Robinfr/electron-react-typescript).

## License

MIT ©