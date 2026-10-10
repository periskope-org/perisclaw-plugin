# Perisclaw

Use your own WhatsApp from Claude and ChatGPT through your Perisclaw account.
Ask what needs your reply, search past messages, and review a drafted reply in
a card before you send it. The card sends each reply at most once.

## Setup

1. Install the plugin. It connects to the Perisclaw MCP server at
   `https://api.perisclaw.com/mcp/plugin`.
2. Sign in on the Perisclaw consent page when your app asks. If your number is
   not linked yet, the same page links it.
3. Choose **Read only** or **Read + write**. You can reconnect later to change it.

## What it runs, sends and fetches

- **No local code.** The plugin contains one skill (`skills/perisclaw-whatsapp`)
  and a reference to one remote MCP server. It runs no hooks, scripts or
  commands on your machine.
- **One remote server.** Every tool call goes to `api.perisclaw.com` over HTTPS
  with the OAuth token from your consent. The token reaches one WhatsApp number.
- **Sends only what you approve.** Replies send when you press Send in the card,
  or after you approve the exact text in the conversation. Read-only
  connections cannot send.
- **Blocked chats stay private.** Chats you block from AI access in Perisclaw are
  refused on the server.

## Example prompts

- What needs my reply on WhatsApp?
- Find the message where someone sent me an address.
- Reply to Bharat that Friday works.

## Privacy and support

- Privacy policy: https://perisclaw.com/legal/privacy-policy
- Terms: https://perisclaw.com/legal/terms-of-service
- Support: https://what.sapp.link/perisclaw
