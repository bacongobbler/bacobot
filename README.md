# bacobot

A Slack bot specifically tailored to run on top of Microsoft Azure Functions.

## Deploying this Project

1. Create an azure function app from the portal or from the CLI using `az functionapp create`
2. Set up git deployment via

```
az functionapp deployment source config --name <appname> --resource-group <rgname> --repo-url https://github.com/bacongobbler/bacobot --branch master --manual-integration
```