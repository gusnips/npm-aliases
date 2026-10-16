# npm-aliases

The `@gusnips/*` names for my npm packages. Each one depends on the real package and re-exports it, so there is one copy of the code.

| Alias                     | Real package        | Range            |
| ------------------------- | ------------------- | ---------------- |
| `@gusnips/assinafy`       | `assinafy`          | `^1.0.0`         |
| `@gusnips/wuzapi`         | `wuzapi`            | `^1.12.0`        |
| `@gusnips/evolution`      | `evolution-api-sdk` | `>=0.7.0 <1.0.0` |
| `@gusnips/falai`          | `@falai/agent`      | `^4.0.0`         |
| `@gusnips/municipios`     | `municipios-brasil` | `>=0.2.1 <1.0.0` |
| `@gusnips/targetdata`     | `targetdata`        | `>=0.1.0 <1.0.0` |
| `@gusnips/netcup`         | `netcup-sdk`        | `>=1.0.0 <2.0.0` |
| `@gusnips/sociavault`     | `sociavault`        | `>=0.1.0 <1.0.0` |
| `@gusnips/scrapecreators` | `scrapecreators`    | `>=0.1.0 <1.0.0` |
| `@gusnips/sherlocker`     | `sherlocker`        | `>=0.1.0 <1.0.0` |

Docs and source stay with the real package. An alias needs a new release only when the real package moves to a new major version. The packages below `1.0.0` use a range that stops at `1.0.0`, so each new `0.x` release reaches the alias by itself.

## Publish

From the alias folder, once per alias:

```bash
cd assinafy
npm publish
```

Every alias starts at `1.0.0` and stays there until its range changes.
