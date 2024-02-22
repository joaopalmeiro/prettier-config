# Notes

- [semantic-release](https://www.npmjs.com/package/semantic-release) package
- `npm view prettier versions`
- [Is it possible to specify where your config file is?](https://github.com/prettier/eslint-plugin-prettier/issues/246#issuecomment-672326840) issue
- [commitlint](https://github.com/conventional-changelog/commitlint) and [@commitlint/config-conventional](https://github.com/conventional-changelog/commitlint/tree/master/@commitlint/config-conventional):
  - [Rules](https://github.com/conventional-changelog/commitlint/tree/master/@commitlint/config-conventional#rules) and [types](https://commitlint.js.org/#/reference-prompt?id=questions)
  - [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/)
  - [Local setup](https://commitlint.js.org/#/guides-local-setup)
  - [CLI options](https://commitlint.js.org/#/reference-cli)
  - Hook: `npx husky add .husky/commit-msg 'npx --no -- commitlint --edit --verbose $1'`
  - [Git Hooks](https://githooks.com/)
- https://prettier.io/docs/en/configuration#configuration-schema: `https://json.schemastore.org/prettierrc`
- https://github.com/prettier/prettier-vscode/tree/v10.1.0?tab=readme-ov-file#prettierrequireconfig-default-false

## Snippets

### `commitlint.config.js`

```js
module.exports = { extends: ['@commitlint/config-conventional'] };
```

### `.husky/commit-msg`

```sh
#!/bin/sh
. "$(dirname "$0")/_/husky.sh"

npx --no -- commitlint --edit --verbose
```