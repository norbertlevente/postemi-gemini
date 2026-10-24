# Postemi extension for Gemini CLI

Write, schedule and publish social media posts from Gemini CLI with
[Postemi](https://postemi.com): Facebook, Instagram, X, LinkedIn, TikTok, YouTube,
Threads, Bluesky, Telegram, Discord, Slack and Pinterest (beta). Postemi previews every post per
account (name, @handle, local publish time, character count) and creates it
only after you confirm.

## Install

```bash
gemini extensions install https://github.com/norbertlevente/postemi-gemini
```

On first use Gemini CLI opens Postemi's sign-in page in your browser. Approve
access for the workspace you want to use.

## What it adds

- MCP server `postemi` at `https://mcp.postemi.com/mcp` (streamable HTTP,
  OAuth 2.1 with dynamic client registration).
- Context file `GEMINI.md` and the skill `postemi`: the posting workflow and
  its rules.
- Commands:
  - `/postemi:announce-release`: posts about your latest release, from the
    changelog.
  - `/postemi:schedule-post <what and when>`: one post, at the time you name.

## Requirements

- A Postemi account at [postemi.com](https://postemi.com) with your social channels
  connected, on a workspace whose plan includes API access.
- A browser on the machine, for the sign-in.

## Try it

- `/postemi:announce-release LinkedIn and X, tomorrow 9:00`
- "What is scheduled on my social channels this week?"
- "Cancel the LinkedIn post for Friday."

## Links

- Documentation: https://postemi.com/docs/mcp
- Privacy: https://postemi.com/privacy
- Support: norbert@postemi.com

License: AGPL-3.0
