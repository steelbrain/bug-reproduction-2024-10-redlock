# Bug Reproduction

```sh
$ yarn
$ yarn tsc -p tsconfig.json --noEmit
index.ts:1:21 - error TS7016: Could not find a declaration file for module 'redlock'. '/Users/aneesiqbal/Projects/steelbrain/bug-reproduction-2024-10-redlock/node_modules/redlock/dist/esm/index.js' implicitly has an 'any' type.
  There are types at '/Users/aneesiqbal/Projects/steelbrain/bug-reproduction-2024-10-redlock/node_modules/redlock/dist/index.d.ts', but this result could not be resolved when respecting package.json "exports". The 'redlock' library may need to update its package.json or typings.

1 import redlock from 'redlock'
                      ~~~~~~~~~


Found 1 error in index.ts:1

error Command failed with exit code 2.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```


As evident from the error message, the "exports" config in package.json is incorrect.
