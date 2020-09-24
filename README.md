# AEM Guides - WKND Asset Compute application

Welcome to the WKND Asset Compute application!

This project contains the example code use to define a custom Asset Compute worker as illustrated in the [Asset Compute extensibility tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/asset-compute/overview.html).

## Setup

- Populate the `.env` file in the project root and fill it as shown [below](#env). Node that the `console.json` file must also contain accurate information for Local Dev.

## Local Dev

- `aio app run` to start your local Dev server
- App will run on `localhost:9000` by default

## Test & Coverage

- Run `aio app test` to run unit tests for ui and actions

## Deploy & Cleanup

- `aio app deploy` to build and deploy all actions on Runtime and static files to CDN
- `aio app undeploy` to undeploy the app

## Config

### `.env`

```bash
# This file must not be committed to source control

## please provide your Adobe I/O Runtime credentials
# AIO_RUNTIME_AUTH=
# AIO_RUNTIME_NAMESPACE=
```

### `manifest.yml`

- List your backend Asset Compute Workers under the `actions` field within the `__APP_PACKAGE__`
package placeholder. We will take care of replacing the package name placeholder
by your project name and version.
- For each action, use the `function` field to indicate the path to the Asset Compute worker code entry point.

## Contributing
Looking to contribute to this project? Please review our [Contributing guidelines](CONTRIBUTING.md) prior to opening a pull request.

We look forward to working with you!

## Licensing
This project is licensed under the Apache V2 License. See [LICENSE](LICENSE) for more information.