# Modern Typescript Monorepo Boilerplate

[For React web application](https://github.com/jarry3369/react-monorepo-boilerplate)  
Template for modern ts projects

## Features

- Pre-configured with VSCode code snippets and other VSCode settings
- Pre-configured with code quality tools: ESLint, Prettier, TypeScript, etc.

## Directory Structure

basically it's monopoe, so additional scripts or servers can be developed in repo

`├──`[`.github`](.github) — GitHub configuration including CI/CD workflows  
`├──`[`.vscode`](.vscode) — VSCode settings, recommended extensions etc.  
`├──`[`app`](./app) — application
`├──`[`env`](./env) — Application settings, API keys, etc.  
`├──`[`scripts`](./scripts) — Automation scripts such as `deploy`  
`├──`[`tsconfig.json`](./tsconfig.json) — The root TypeScript configuration  
`└──`[`tsconfig.base.json`](./tsconfig.base.json) — The common/shared TypeScript configuration

## Tech Stack

- [TypeScript](https://www.typescriptlang.org/), [ESLint](https://eslint.org/), [Prettier](https://prettier.io/), [PNPm](https://pnpm.io/)

## Requirements

- [Node.js](https://nodejs.org/) v18+ with [Corepack](https://nodejs.org/api/corepack.html) (`$ corepack enable`)
- [VS Code](https://code.visualstudio.com/) editor with [recommended extensions](.vscode/extensions.json)
- Optionally [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)
  and [Reactime](https://chrome.google.com/webstore/detail/reactime/cgibknllccemdnfhfpmjhffpjfeidjga?hl=en) browser extensions

## Getting Started

[Generate](https://github.com/jarry3369/modern-typescript-monorepo-boilerplate) a new project
from this template, clone, install dependencies, update the
environment variables found in [`env/*.env`](./env/), and enjoy party :

```bash
$ git clone https://github.com/jarry3369/modern-typescript-monorepo-boilerplate.git [app_name]
$ cd [app_name]

# can spell just `pnpm i`
$ pnpm install
$ pnpm dev
```

**IMPORTANT**: Ensure that VSCode is using the workspace [version of TypeScript](https://code.visualstudio.com/docs/typescript/typescript-compiling#_using-newer-typescript-versions)
and ESLint.

![](https://files.tarkus.me/typescript-workspace.png)

add dependencies for party,

```bash
# This command will install Package on root
$ pnpm add -w <NODE_PACKAGE_NAME>
# If you want to add a dependency for special Repo,
$ pnpm add --filter <MONOREPO_PACKAGE_NAME> <NODE_PACKAGE_NAME>
```

wanna remove dependencies from party,

```bash
# When used inside a workspace, removes a dependency (or dependencies) from every workspace package.
# can spell 'rm' or 'uninstall' or 'un' as well
$ pnpm remove -r <NODE_PACKAGE_NAME>
# If you want to remove dependency for special Repo,
$ pnpm remove --filter <MONOREPO_PACKAGE_NAME> <NODE_PACKAGE_NAME>
```

[check more infomations here](https://pnpm.io/cli/add)

## Scripts

- `pnpm dev` — Launches the app in development env
- `pnpm preview` — Launches the app in production env
- `pnpm test` — Run unit tests
- `pnpm build` — Run build for all projects in repository.
- `pnpm workspace <WORKSPACE-NAME> [-rm]` - Create additional workspaces with configurations. [-rm] flag will remove target workspace from the repository.

## How to Deploy

Ensure that all the environment variables for the target deployment environment in [`/env/*.env`](./env/) files are up-to-date.

```
$ pnpm build
- theres no automation deploy yet, but _will be update_
```

## License

[Copyright © 2025 @jarry3369](https://github.com/jarry3369/modern-typescript-monorepo-boilerplate/blob/main/LICENSE)
