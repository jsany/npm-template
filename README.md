<h1 align="center">Welcome to @jsany/npm-template 👋</h1>
<p>
  <a href="https://www.npmjs.com/package/npm-template">
    <img alt="Version" src="https://img.shields.io/npm/v/npm-template.svg">
  </a>
  <a href="https://github.com/jsany/npm-template#readme">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" target="_blank" />
  </a>
  <a href="https://github.com/jsany/npm-template/graphs/commit-activity">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" target="_blank" />
  </a>
  <a href="https://github.com/jsany/npm-template/blob/master/LICENSE">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" target="_blank" />
  </a>
</p>

> npm pkg typescript template

### 🏠 [Homepage](https://github.com/jsany/npm-template#readme)

## Feature

- [x] **typescript**
- [x] **eslint**
- [x] **@typescript-eslint**
- [x] **no-tslint**
- [x] **prettier**
- [x] **standard-version**
- [x] **unit-test(jest)**
- [x] **commit convention**
- [x] **react component / jsx**

## Install

```sh
npm install
```

## Usage

```sh
npm run start
```

## Run tests

```sh
npm run test
```

## Publish Steps

### 1. Login

```sh
npm login
```

### 2. Version(control)

#### First Release

To generate your changelog for your first release, simply do:

```sh
npm run release -- --first-release
```

This will tag a release without bumping the version in package.json (et al.).

When ready, push the git tag and npm publish your first release.

#### Cut a Release

If you typically use `npm version` to cut a new release, do this instead:

```sh
npm run release
```

As long as your git commit messages are conventional and accurate, you no longer need to specify the semver type - and you get CHANGELOG generation for free!

After you cut a release, you can push the new git tag and `npm publish` (or `npm publish --tag next`) when you're ready.

#### Release as a pre-release

Use the flag `--prerelease` to generate pre-releases:

Suppose the last version of your code is `1.0.0`, and your code to be committed has patched changes. Run:

```sh
npm run release -- --prerelease
```

you will get version `1.0.1-0`.

If you want to name the pre-release, you specify the name via `--prerelease <name>`.

For example, suppose your pre-release should contain the `alpha` prefix:

```sh
npm run release -- --prerelease alpha
```

this will tag the version `1.0.1-alpha.0`

#### Release as a target type imperatively like npm version

To forgo the automated version bump use `--release-as` with the argument `major`, `minor` or `patch`:

Suppose the last version of your code is `1.0.0`, you've only landed `fix:` commits, but you would like your next release to be a `minor`. Simply do:

```sh
npm run release -- --release-as minor
# or
npm run release -- --release-as 1.1.0
```

you will get version `1.1.0` rather than the auto generated version `1.0.1`.

> NOTE: you can combine `--release-as` and `--prerelease` to generate a release. This is useful when publishing experimental feature(s).

#### Prevent Git Hooks

If you use git hooks, like pre-commit, to test your code before committing, you can prevent hooks from being verified during the commit step by passing the `--no-verify` option:

```sh
npm run release -- --no-verify
```

### 3. Npm publish

```sh
npm publish
# or public pkg
npm publish --access=public
```

## Author

👤 **jiangzhiguo2010**

- Github: [@jsany](https://github.com/jsany)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/jsany/npm-template/issues).

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2019 [jiangzhiguo2010](https://github.com/jsany).<br />
This project is [MIT](https://github.com/jsany/npm-template/blob/master/LICENSE) licensed.

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
