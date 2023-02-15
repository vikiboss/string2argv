## string2argv

Parse a string into an argument array, do the job like `process.argv` for us.

This is a fork from [string-argv](https://github.com/mccormicka/string-argv), changes in this fork:

- rename package to [`string2argv`](https://npm.im/string2argv).
- export extra `string2argv` & `str2argv` aliases.
- change `export { xx as default }` to `export default xx`.
- compatible with both **ESM** and **CJS** (by the change above).

### Usage

**ESM**

```js
import { string2argv } from 'string2argv'

const commandLineString = 'echo a b c -rvf --name "demo name"'

// output: [ 'echo', 'a', 'b', 'c', '-rvf', '--name', 'demo name' ]
console.log(string2argv(commandLineString))
```

**CJS**

```js
const { default: string2argv } = require('string2argv')

const commandLineString = 'echo a b c -rvf --name "demo name"'

// output: [ 'echo', 'a', 'b', 'c', '-rvf', '--name', 'demo name' ]
console.log(string2argv(commandLineString))
```
