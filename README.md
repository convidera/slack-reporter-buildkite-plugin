# Slack Reporter Buildkite Plugin

Reports status to Slack before/after a Buildkite step is executed.

## Example

Add the following to your `pipeline.yml`:

```yml
steps:
  - command: echo 'Deploy preview created'
    plugins:
      - convidera/slack-reporter#v1.0.0:
        token: SLACK_TOKEN
        channel: SLACK_CHANNEL
```

## Configuration

- `token` - Name of env var containing Slack token

- `channel` - Name of env var containing Slack ChannelID

## Developing

To lint the `plugin.yml` file:

```sh
docker-compose run --rm lint
```

To run the tests:

```shell
docker-compose run --rm tests
```
