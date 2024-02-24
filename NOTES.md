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
- [Sharing configurations](https://prettier.io/docs/en/configuration.html#sharing-configurations) documentation
- [Configuration Overrides](https://prettier.io/docs/en/configuration.html#configuration-overrides) documentation
- https://yarnpkg.com/cli/add#options
- https://pnpm.io/cli/add#--save-dev--d
- https://bun.sh/docs/cli/add#dev
- https://github.com/prettier/prettier/releases
- https://prettier.io/blog/
- https://prettier.io/blog/2024/01/12/3.2.0.html
- https://npmpackagejsonlint.org/docs/cli
- https://docs.npmjs.com/cli/v10/configuring-npm/package-json#repository
- https://nodejs.org/api/packages.html#type
- https://github.com/snyk-snippets/modern-npm-package/blob/main/package.json
- https://github.com/joaopalmeiro/npm-package-json-lint-config-package

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

### `.github/workflows/npm-publish.yml`

```yml
# Source:
# - https://github.com/actions/starter-workflows/blob/main/ci/npm-publish.yml
# - https://github.com/egoist/prettier-config/blob/master/.github/workflows/node.js.yml
# - https://github.com/actions/setup-node
# - https://typicode.github.io/husky/#/?id=disable-husky-in-cidocker
# - https://docs.github.com/en/actions/publishing-packages/publishing-nodejs-packages#publishing-packages-to-the-npm-registry
# - https://docs.npmjs.com/creating-and-publishing-scoped-public-packages#publishing-scoped-public-packages
name: Node.js Package

on:
  push:
    tags:
      - 'v*'

jobs:
  publish-npm:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-node@v2
        with:
          node-version: '16.13.1'
          registry-url: 'https://registry.npmjs.org/'
      - run: npm ci --omit=dev --ignore-scripts
      - run: npm publish --access public
        env:
          NODE_AUTH_TOKEN: ${{secrets.npm_token}}
```

## Commands

```bash
npm install -D prettier publint sort-package-json npm-run-all2 npm-package-json-lint npm-package-json-lint-config-package
```
