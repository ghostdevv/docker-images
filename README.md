# Docker Images

A collection of modififed/custom docker images I frequently use. All are built/automatically updated twice a month by GitHub actions and published to the ghcr.

## Node

Modified version of the [official node images](https://hub.docker.com/_/node). Package managers will always be on the latest version for the node you're using.

| Node Version | Base Image              | Package Managers           | Extra        |
| ------------ | ----------------------- | -------------------------- | ------------ |
| 20           | `node:20-bullseye-slim` | `npm@10`, `pnpm@8`, `yarn` | `tsm@latest` |
| 18           | `node:18-bullseye-slim` | `npm@10`, `pnpm@8`, `yarn` | `tsm@latest` |
| 16           | `node:16-bullseye-slim` | `npm@9`, `pnpm@8`, `yarn`  | `tsm@latest` |

```Dockerfile
FROM ghcr.io/ghostdevv/node:VERSION

# ...
```
