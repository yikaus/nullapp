# nullapp

[![](https://github.com/yikaus/nullapp/workflows/CI/badge.svg)](https://github.com/yikaus/nullapp/actions/)

A minimal AWS Lambda application managed with the Serverless Framework. Includes multiple CI/CD configurations and a simple handler function.
[DONE BY github MCP server docker version]
## Features
- **AWS Lambda**: Simple handler returning a message
- **Serverless Framework**: Easy deployment to AWS
- **CI/CD**: GitHub Actions, Drone CI, and Dagger for build/test automation
- **Funding**: [Support via PayPal](https://www.paypal.me/yikaus)

## Getting Started

### Prerequisites
- Node.js (v12 or later)
- Serverless Framework (`npm install -g serverless`)
- AWS credentials configured

### Deploy
```sh
sls deploy
```

### Test Locally
```sh
sls invoke local -f hello
```

## CI/CD
- **GitHub Actions**: See `.github/workflows/null.yml` for automated tests on push to `master`.
- **Drone CI**: `.drone.yml` for alternative CI pipeline.
- **Dagger**: `dagger.cue` for advanced build/test automation.

## Handler Example
```js
module.exports.hello = async event => {
  return { message: 'nullapp!', event };
};
```

## License
MIT
