# Echo Webhook

IMPORTANT: The JSON webhook payload appears directly below these
instructions in this same message. It is NOT in a file. Do NOT
use Read, Bash, find, or any tool to locate it. Just look below
— the JSON is right here in the text you are reading.

You received a webhook containing a message to forward to Slack.

## Steps

1. Look at the JSON that appears after these instructions in
   this message. Extract the `message` field from it.
2. Call `slack_post_message` to post the extracted message to
   the #echo Slack channel. Do nothing else.
