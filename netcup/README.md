# @gusnips/netcup

The same Netcup CLI and typed JavaScript client as [`netcup-sdk`](https://www.npmjs.com/package/netcup-sdk).

```sh
npx @gusnips/netcup --help
```

Requires Node.js 22.0.0 or newer. Alias `2.0.0` uses core `>=1.0.0 <2.0.0`. This raises the Node minimum from the previous core's 18.3 requirement. Alias `1.2.0` keeps its `<1.0.0` core range and does not pick up that runtime change.

For servers, sign in with `npx @gusnips/netcup login`. Domains and DNS use a separate API key:

```sh
npx @gusnips/netcup ccp login
bunx @gusnips/netcup ccp domains list
```

Get the key from CCP > Master Data > API. Input is hidden. Saved credentials are plaintext files; keep them private. DNS changes follow prepare, review and explicit commit steps. The CLI does not use the legacy CCP JSON API.

## Use with an AI client

The alias forwards `netcup mcp` too. For a reviewed setup, pin the core package so the launch does not move with the alias's dependency range:

```sh
npx --yes netcup-sdk@1.0.0 mcp
```

Or use `bunx netcup-sdk@1.0.0 mcp`. Standard `bunx` uses Node for this executable. The AI client starts and owns a local stdio process; no clone, build step or server port is needed.

MCP has nine fixed read-only tools for selected server, task, domain and DNS data. It cannot change servers or DNS. Run the matching SCP or CCP login outside the AI client first. MCP reuses that saved login, with environment credentials taking precedence. It never opens an auth prompt. If login fails, run the matching CLI login and reconnect the client.

[Client setup, tools and privacy limits](https://github.com/gusnips/netcup#use-with-an-ai-client).

## Install or import

For a global install, choose this package or `netcup-sdk`, not both. Both provide the `netcup` command.

Library imports still work:

```ts
import { NetcupClient, NetcupCcpClient } from "@gusnips/netcup";
```

[Commands, login and SDK docs](https://github.com/gusnips/netcup#readme).

[Source and issues](https://github.com/gusnips/netcup).
