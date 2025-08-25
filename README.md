# Vanilla JavaScript App

[Azure Static Web Apps](https://docs.microsoft.com/azure/static-web-apps/overview) allows you to easily build JavaScript apps in minutes. Use this repo with the [quickstart](https://learn.microsoft.com/en-us/azure/static-web-apps/deploy-web-framework?tabs=bash&pivots=vanilla-js) to build and customize a new static site.

This repo features a Azure CLI driven infrastructure setup script that creates
the resource group and the static web app in Azure. It therefore automates the
first half of the quickstart page above. Find the script in the subfolder `infra`.

This repo is used as a starter for a _very basic_ HTML web application using no front-end frameworks.

This repo has a dev container. This means if you open it inside a [GitHub Codespace](https://github.com/features/codespaces), or using [VS Code with the remote containers extension](https://code.visualstudio.com/docs/remote/containers), it will be opened inside a container with all the dependencies already installed.

## Quickstart Synopsis

```bash
az login
az account set --subscription  "<SUBSCRIPTION_NAME_OR_ID>"
infra/provision.sh
npm install -D @azure/static-web-apps-cli
npx swa init --yes
npx swa login --resource_group rg-vanilla-basic-cli-swa --app_anem stapp-vanilla-basic-cli-swa
npx swa deploy --env production

(optionally) az group delete rg-vanilla-basic-cli-swa
```
