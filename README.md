<p align="center">
  <a href="https://postemi.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="assets/postemi-logo-white.svg">
      <img src="assets/postemi-logo-black.svg" alt="Postemi" height="56">
    </picture>
  </a>
</p>

# Postemi extension for Gemini CLI

Write, schedule and publish social media posts from Gemini CLI with
[Postemi](https://postemi.com), the social media scheduler for 37 platforms
and apps: Instagram, TikTok, Facebook, LinkedIn, X, YouTube, Threads,
Bluesky, Pinterest, Discord, Telegram, Slack, Mastodon, blogs, team chats,
newsletters and more. Postemi previews every post per account (name,
@handle, local publish time, character count) and creates it only after you
confirm.

## Install

```bash
gemini extensions install https://github.com/norbertlevente/postemi-gemini
```

Then start Gemini CLI and run `/mcp auth postemi`. Postemi's sign-in page
opens in your browser; approve access for the workspace you want to use.
There is no key to paste.

## What it adds

- MCP server `postemi` at `https://mcp.postemi.com/mcp` (streamable HTTP,
  OAuth 2.1 with dynamic client registration).
- Context file `GEMINI.md`: the main Postemi skill, with the tools, the
  posting workflow and its rules (preview before create, times in your
  timezone, the real character limit of each account).
- Skills:
  - `postemi-writing`: post ideas, hooks and headlines, the writing rules of
    each network, a check before publishing.
  - `postemi-templates`: the template and hook library of the Postemi
    composer, with [placeholders] to fill.
  - `postemi-growth`: a niche, a 30-day posting test, cadence per network,
    reading the numbers, a content plan and a weekly review.
- Commands:
  - `/postemi:announce-release`: posts about your latest release, from the
    changelog.
  - `/postemi:schedule-post <what and when>`: one post, at the time you name.

## Requirements

- A Postemi account at [postemi.com](https://postemi.com) with your social
  channels connected, on a workspace whose plan includes API and MCP access
  (Pro, Creator or Team). Every plan starts with a 7-day free trial.
- A browser on the machine, for the sign-in.

## Try it

- `/postemi:announce-release LinkedIn and X, tomorrow 9:00`
- "Write a LinkedIn post about our new pricing page and schedule it for Tuesday 8:30."
- "What is scheduled on my social channels this week?"
- "Make me a 30-day content plan for Instagram and TikTok."
- "Cancel the LinkedIn post for Friday."

## Privacy and network endpoints

The extension connects only to Postemi:

- `https://mcp.postemi.com/mcp`: the hosted MCP server
- `https://mcp.postemi.com/.well-known/oauth-authorization-server`: OAuth
  metadata, with client registration, token and revoke endpoints on the same
  host
- `https://postemi.com/app/oauth/authorize`: the sign-in and consent page

Gemini CLI stores the OAuth token; no key is stored in the extension. Tools
act only on the workspace you approved. Social accounts are connected in
Postemi itself, never through the extension. The extension ships no hooks
and runs no code on your machine.

## Links

- Documentation: https://postemi.com/docs/mcp
- Other AI clients and the CLI: https://github.com/norbertlevente/postemi-agent
- Privacy: https://postemi.com/privacy
- Terms: https://postemi.com/terms
- Support: norbert@postemi.com

## License

AGPL-3.0 (see [LICENSE](./LICENSE) and [NOTICE](./NOTICE)). Use of the
hosted service is governed by Postemi's terms: https://postemi.com/terms
