# @gusnips/netcup

The same Netcup CLI and typed JavaScript client as [`netcup-sdk`](https://www.npmjs.com/package/netcup-sdk).

```sh
npx @gusnips/netcup --help
```

For servers, sign in with `npx @gusnips/netcup login`. Domains and DNS use a separate API key:

```sh
npx @gusnips/netcup ccp login
bunx @gusnips/netcup ccp domains list
```

Get the key from CCP > Master Data > API. Input is hidden. DNS changes follow prepare, review and explicit commit steps. The CLI does not use the legacy CCP JSON API or include MCP support.

For a global install, choose this package or `netcup-sdk`, not both. Both provide the `netcup` command.

Library imports still work:

```ts
import { NetcupClient, NetcupCcpClient } from "@gusnips/netcup";
```

[Commands, login and SDK docs](https://github.com/gusnips/netcup#readme).

[Source and issues](https://github.com/gusnips/netcup).
