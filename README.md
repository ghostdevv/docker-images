# Docker Images

A collection of modififed/custom docker images I frequently use. All are built/automatically updated twice a month by GitHub actions and published to the ghcr.

## Node

Modified version of the [official node images](https://hub.docker.com/_/node). Package managers will always be on the latest version for the node you're using.

| Tag       | Base Image              | Package Managers           | Extra        |
| --------- | ----------------------- | -------------------------- | ------------ |
| 22        | `node:22-bookworm-slim` | `npm@10`, `pnpm@9`, `yarn` | `tsm@2` |
| 20        | `node:20-bookworm-slim` | `npm@10`, `pnpm@8`, `yarn` | `tsm@2` |
| 18        | `node:18-bookworm-slim` | `npm@10`, `pnpm@8`, `yarn` | `tsm@2` |
| 16        | `node:16-bullseye-slim` | `npm@9`, `pnpm@8`, `yarn`  | `tsm@2` |
| 22-alpine | `node:22-alpine`        | `npm@10`, `pnpm@9`, `yarn` | `tsm@2` |
| 20-alpine | `node:20-alpine`        | `npm@10`, `pnpm@8`, `yarn` | `tsm@2` |
| 18-alpine | `node:18-alpine`        | `npm@10`, `pnpm@8`, `yarn` | `tsm@2` |
| 16-alpine | `node:16-alpine`        | `npm@9`, `pnpm@8`, `yarn`  | `tsm@2` |

-   Default workdir: `/app`
-   Platforms: `amd64`, `arm64`

```Dockerfile
FROM ghcr.io/ghostdevv/node:TAG
```

<details>
<summary>Example: Run a Discord bot</summary>

```Dockerfile
FROM ghcr.io/ghostdevv/node:22-alpine

RUN git clone https://github.com/sveltejs/discord-bot /app
RUN pnpm install

CMD [ "pnpm", "start" ]
```

</details>
