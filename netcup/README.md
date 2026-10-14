# @gusnips/netcup

The same Netcup command and JavaScript client as [`netcup-sdk`](https://www.npmjs.com/package/netcup-sdk).

```sh
npx @gusnips/netcup servers get 12345
```

Sign in first with `npx @gusnips/netcup login`. Bun works too:

```sh
bunx @gusnips/netcup --help
```

For a global install, choose this package or `netcup-sdk`, not both. Both provide the `netcup` command.

Library imports still work:

```ts
import { NetcupClient } from "@gusnips/netcup"; // or "netcup-sdk"
```

[Commands, login and SDK docs](https://github.com/gusnips/netcup#readme).

[Source and issues](https://github.com/gusnips/netcup).
