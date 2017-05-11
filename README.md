# bacobot

A Slack bot specifically tailored to run on top of Microsoft Azure Functions.

## Deploying this Project

1. Create an azure function app from the portal or from the CLI using `az functionapp create`
2. Set up git deployment via

```
az functionapp deployment source config --name <appname> --resource-group <rgname> --repo-url https://github.com/bacongobbler/bacobot --branch master --manual-integration
```

3. Create a Slack webhook URL using https://my.slack.com/services/new/incoming-webhook
4. POST to the function app with the following body

```
{
    "channel": "<channel>",
    "username": "<botname>",
    "text": "Hello, World!",
    "icon_url": "",
    "icon_emoji": ":lightning_cloud:",
    "fallback": "Upgrade your client",
    "notifications": []
}
```