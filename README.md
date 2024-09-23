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

#### Getting Started

1. Navigate to:  https://github.com/ernestgwilsonii/baseDevKit
2. Click the the down arrow on the green "Code" button
3. Click: "Open with GitHub Desktop"
4. When GitHub Desktop opens, click: "Open in Visual Studio Code"
5. When Visual Studio Code opens, open the command palette and click: "Dev Containers:"

#### Recommended Visual Studio Code Extensions

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
- [markdownlint](marketplace.visualstudio.com/items?itemName=davidanson.vscode-markdownlint)
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

# Added additional packages
sudo ./packages.sh

# Configure AWS
aws configure

# Confirm AWS
aws sts get-caller-identity
```

#### Running

```bash
# TBD
# Create your local .env with non-git variables
#echo "TOKEN="12345" >> .env

# Example adding Python packages:
#pip install python-dotenv
#pip freeze > requirements.txt

# Install Python required modules
#pip install -r requirements.txt
```
