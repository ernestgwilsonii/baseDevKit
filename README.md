### Docker in Docker Development Kit

TL;DR: This is a basic development environment that is the starting place for other projects.

#### Prerequisites

- [GitHub](https://github.com) Account
- Git related tools:
  - [SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) setup for your workstation and configured in your GitHub account
  - [git](https://git-scm.com/downloads) client CLI (also adds Git BASH)
  - [GitHub Desktop](https://desktop.github.com/download/)
  - [GitHub CLI](https://cli.github.com)
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
- [Docker](https://docs.docker.com/get-started/get-docker/)
- [Visual Studio Code](https://code.visualstudio.com)

```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

#### Getting Started

1. Navigate to:  https://github.com/ernestgwilsonii/baseDevKit
2. Click the the down arrow on the green "Code" button
3. Click: "Open with GitHub Desktop"
4. When GitHub Desktop opens, click: "Open in Visual Studio Code"
5. When Visual Studio Code opens, open the command palette and click: "Dev Containers: Open Folder in Container"

#### Included Visual Studio Code Extensions

- [Amazon Q](https://marketplace.visualstudio.com/items?itemName=AmazonWebServices.amazon-q-vscode)
- [C/C++ Themes](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-themes) by Microsoft
- [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools) by Microsoft
- [C# Dev Kit](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csdevkit) by Microsoft
- [C#](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
- [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) by Microsoft
- [ES7+ React/Redux/React-Native snippets](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) by Microsoft
- [Extension Pack for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) by Microsoft
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) Git supercharged
- [Go](https://marketplace.visualstudio.com/items?itemName=golang.Go)
- [GraphQL](https://marketplace.visualstudio.com/items?itemName=GraphQL.vscode-graphql): Language Feature Support
- [Import Cost](https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost)
- [JavaScript and TypeScript Nightly](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-next) by Microsoft
- [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
- [Node.js Modules Intellisense](https://marketplace.visualstudio.com/items?itemName=leizongmin.node-module-intellisense)
- [npm Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense)
- [PlatformIO IDE](https://marketplace.visualstudio.com/items?itemName=platformio.platformio-ide)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) Code formatter
- [Prisma NextJS](https://marketplace.visualstudio.com/items?itemName=WillLuke.nextjs)
- [Prisma](https://marketplace.visualstudio.com/items?itemName=Prisma.prisma)
- [Python Debugger](https://marketplace.visualstudio.com/items?itemName=ms-python.debugpy) by Microsoft
- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) by Microsoft
- [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) by Microsoft
- [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)
- [rust](https://marketplace.visualstudio.com/items?itemName=1YiB.rust-bundle)
- [SQLite](https://marketplace.visualstudio.com/items?itemName=alexcvzz.vscode-sqlite)
- [Tailwind CSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)
- [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight)

#### Setup

- How to [forward ports](https://code.visualstudio.com/docs/editor/port-forwarding)

```bash
# Check versions installed by .devcontainer/devcontainer.json
aws --version
cargo --version
docker -v
docker-compose -v
dotnet --info
go version
gradle --version
java --version
javac --version
node -v
npx -v
pip --version
python -V
rustc --version

# Configure AWS
aws configure

# Confirm AWS
aws sts get-caller-identity
```

#### Running

```bash
# Create Next.js app in the current directory naming it: "next-with-cognito"
# REF: https://nextjs.org
npx create-next-app@latest next-with-cognito --use-npm
# `vscode ➜ /workspaces/baseDevKit (NextAmplify) $ npx create-next-app@latest next-with-cognito --use-npm
# ✔ Would you like to use TypeScript? … No / Yes
# ✔ Would you like to use ESLint? … No / Yes
# ✔ Would you like to use Tailwind CSS? … No / Yes
# ✔ Would you like to use `src/` directory? … No / Yes
# ✔ Would you like to use App Router? (recommended) … No / Yes
# ✔ Would you like to customize the default import alias (@/*)? … No / Yes
# Creating a new Next.js app in /workspaces/baseDevKit/next-with-cognito.

# Using npm.

# Initializing project with template: app-tw 


# Installing dependencies:
# - react
# - react-dom
# - next

# Installing devDependencies:
# - typescript
# - @types/node
# - @types/react
# - @types/react-dom
# - postcss
# - tailwindcss
# - eslint
# - eslint-config-next

# npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
# npm warn deprecated rimraf@3.0.2: Rimraf versions prior to v4 are no longer supported
# npm warn deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported
# npm warn deprecated @humanwhocodes/object-schema@2.0.3: Use @eslint/object-schema instead
# npm warn deprecated @humanwhocodes/config-array@0.13.0: Use @eslint/config-array instead

# added 361 packages, and audited 362 packages in 3m

# 137 packages are looking for funding
#   run `npm fund` for details

# found 0 vulnerabilities
# Success! Created next-with-cognito at /workspaces/baseDevKit/next-with-cognito`

git config --global --add safe.directory /workspaces/baseDevKit

cd next-with-cognito

docker-compose build

docker-compose up
```
