# semantic-release-mattermost

semantic-release plugin to get release notifications on mattermost via webhooks

## Install

Add the plugin to your npm-project

### NPM

```shell
npm install plk-semantic-release-mattermost
```

### Yarn

```shell
yarn add plk-semantic-release-mattermost
```

## Usage

Add the plugin to your semantic-release config:

```json
{
  "plugins": [
    "@semantic-release/release-notes-generator",
    [
      "plk-semantic-release-mattermost",
      {
        "webhook": "https://mattermost.example.com",
        "username": "semantic-release",
        "name": "project name"
      }
    ]
  ]
}
```

### Environment variable

If the ```MATTERMOST_WEBHOOK``` environment variable is defined in your environment,
it will be used instead of the ```webhook``` provided in the config.

If the ```CI_PROJECT_NAME``` environment variable is defined in your environment,
it will be used instead of the ```name``` provided in the config.
