# `@joaopalmeiro/prettier-config`

My personal [Prettier](https://prettier.io) config.

- [Source code](https://github.com/joaopalmeiro/prettier-config)
- [npm package](https://www.npmjs.com/package/@joaopalmeiro/prettier-config)
- [Licenses](https://licenses.dev/npm/%40joaopalmeiro%2Fprettier-config/0.1.1)

## Getting Started

### Installation

```bash
npm install --save-dev @joaopalmeiro/prettier-config
```

or

```bash
yarn add --dev @joaopalmeiro/prettier-config
```

or

```bash
pnpm add --save-dev @joaopalmeiro/prettier-config
```

or

```bash
bun add --dev @joaopalmeiro/prettier-config
```

### Usage

To use this configuration, choose one of the options below.

#### Edit the `package.json` file

```json
{
  "prettier": "@joaopalmeiro/prettier-config"
}
```

#### Create a `.prettierrc` file

```json
"@joaopalmeiro/prettier-config"
```

## References

Check out the [Awesome Prettier](https://gitlab.com/joaommpalmeiro/awesome-prettier) repo, please.

## Development

Install [fnm](https://github.com/Schniz/fnm) (if necessary).

```bash
fnm install && fnm use && node --version && npm --version
```

```bash
npm install
```

```bash
npm run lint
```

```bash
npm run format
```

## Deployment

```bash
npm pack --dry-run
```

```bash
npm version patch
```

```bash
npm version minor
```

```bash
npm version major
```

- Update the version in the `Licenses` link at the top.
- Commit and push changes.
- Create a tag on [GitHub Desktop](https://github.blog/2020-05-12-create-and-push-tags-in-the-latest-github-desktop-2-5-release/).
- Check [GitHub](https://github.com/joaopalmeiro/prettier-config).

```bash
npm login
```

```bash
npm publish --access public
```

- Check [npm](https://www.npmjs.com/package/@joaopalmeiro/prettier-config).
