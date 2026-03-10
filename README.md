# Echo

Echo is a [Valet](https://valet.dev) agent for end-to-end testing. It receives messages via webhook or Telegram and forwards them to the **#echo** Slack channel, confirming that the full pipeline — channel to agent to connector to Slack — is working.

## How it works

1. A message arrives through one of the agent's channels (webhook or Telegram).
2. The agent extracts the message content from the payload.
3. The message is posted to **#echo** on Slack exactly as received, with no modifications.

## Channels

| Channel | Type | Description |
|---------|------|-------------|
| `webhook` | Webhook | Accepts JSON payloads with a `message` field |
| `echo-tg` | Telegram | Accepts Telegram messages |

## Connectors

| Connector | Description |
|-----------|-------------|
| `slack` | Slack MCP server for posting messages to the #echo channel |

## Secrets

| Name | Description |
|------|-------------|
| `SLACK_BOT_TOKEN` | Slack bot token (`xoxb-...`) with `chat:write` scope |
| `SLACK_TEAM_ID` | Slack workspace team ID |

## Project structure

```
SOUL.md              # Agent identity and behavior
valet.yaml           # Agent configuration
channels/
  webhook.md         # Instructions for handling webhook messages
  echo-tg.md         # Instructions for handling Telegram messages
```

## License

Apache 2.0 — see [LICENSE](LICENSE) for details.
