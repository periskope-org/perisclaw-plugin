# Security policy

## Reporting a vulnerability

Email **support@periskope.app** with "Security" in the subject. Include the
affected component (this plugin, the MCP server at
`https://api.perisclaw.com/mcp/plugin`, or the Perisclaw web app), steps to
reproduce, and the impact you observed. Please do not open a public GitHub
issue for a vulnerability, and do not test against accounts or WhatsApp numbers
that are not yours.

We will acknowledge your report, keep you updated while we investigate, and
let you know when a fix is live.

## Supported versions

Only the latest version on the default branch is supported. The plugin has no
local code to patch: fixes to the MCP server apply to every user as soon as
they are deployed.

## Security model

- **No local code.** The plugin contains one skill and a reference to one
  remote MCP server. It runs no hooks, scripts or commands on your machine and
  contains no secrets.
- **OAuth sign-in.** Every tool call goes to `api.perisclaw.com` over HTTPS
  with the OAuth token from your consent. A token reaches only your own
  WhatsApp number.
- **Read only unless you choose otherwise.** On the consent screen you pick
  **Read only** or **Read & write**. Read-only connections can search and read
  but cannot send or change anything. Approving a wider grant signs the
  client's older sessions out.
- **Sends are gated.** Replies send only when you press Send in the reply card
  or approve the exact text in the conversation. Chats you block from AI access
  in Perisclaw are refused on the server.
- **Revoke anytime.** Remove a connection from the Perisclaw web app and the
  client loses access immediately.

More detail: https://docs.perisclaw.com/mcp-server and
https://docs.perisclaw.com/privacy-and-security
