# `@joaopalmeiro/prettier-config`

> My personal [Prettier](https://prettier.io) config.

## Usage

**Install**:

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

**Edit `package.json`**:

```json
{
  "prettier": "@joaopalmeiro/prettier-config"
}
```

## References

- [@egoist/prettier-config](https://github.com/egoist/prettier-config) package.
- [@yuler/prettier-config](https://github.com/yuler/prettier-config) package.
- [@azz/prettier-config](https://github.com/azz/prettier-config) package.
- [Sharing configurations](https://prettier.io/docs/en/configuration.html#sharing-configurations) documentation.
- [@zestia/prettier-config](https://github.com/zestia/prettier-config) package.
- [Configuration Overrides](https://prettier.io/docs/en/configuration.html#configuration-overrides) documentation.

## Development

- `npm install`.
- `npm pack --dry-run`.

## Deployment

- `npm version minor` or `npm version patch` or `npm version major`.
- `git push --follow-tags`.

## Notes

- [semantic-release](https://www.npmjs.com/package/semantic-release) package.
- `npm view prettier versions`.
- [Is it possible to specify where your config file is?](https://github.com/prettier/eslint-plugin-prettier/issues/246#issuecomment-672326840) issue.
- [commitlint](https://github.com/conventional-changelog/commitlint) and [@commitlint/config-conventional](https://github.com/conventional-changelog/commitlint/tree/master/@commitlint/config-conventional):
  - [Rules](https://github.com/conventional-changelog/commitlint/tree/master/@commitlint/config-conventional#rules) and [types](https://commitlint.js.org/#/reference-prompt?id=questions).
  - [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/).
  - [Local setup](https://commitlint.js.org/#/guides-local-setup).
  - [CLI options](https://commitlint.js.org/#/reference-cli).
  - Hook: `npx husky add .husky/commit-msg 'npx --no -- commitlint --edit --verbose $1'`.
  - [Git Hooks](https://githooks.com/).
