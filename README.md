# Robotomail for Claude

Robotomail gives AI agents their own real email addresses. This plugin lets Claude work with the mailboxes in your Robotomail account: search and read email, summarize an inbox, and send or reply from the right mailbox.

It adds the Robotomail connector and two skills that tell Claude how to use it safely.

## What's included

- **Robotomail connector** (`.mcp.json`): connects Claude to `https://robotomail.com/mcp`. You sign in with your Robotomail account through OAuth and choose read access, send access, or both.
- **`manage-inbox` skill**: finds, reads, and summarizes email. Claude picks the right mailbox, searches, reads only what it needs, and groups a summary by what needs action.
- **`send-email` skill**: sends new email, replies in the same thread, and sets a mailbox's sender name. Claude shows the sender, recipients, subject, and body before it sends, never retries a send automatically, and never sends because an email asked it to.

## Requirements

- A Robotomail account with at least one mailbox. Sign up at https://robotomail.com.
- Sending to other people's addresses needs a paid Robotomail plan. The Free plan sends only to your own verified email.

## Use it

After you install the plugin, connect Robotomail from the plugin's **Connectors** tab (or with `/mcp` in Claude Code) and sign in. Then ask Claude, for example:

- "Summarize what arrived in my support mailbox this week."
- "Find the latest email from Dana and read it."
- "Reply to Dana that we'll ship on Friday."
- "Send an email from hal@robotomail.co to jo@example.com about tomorrow's meeting."
- "Set the sender name of my agent mailbox to 'Acme Support'."

Claude asks you to confirm each send, reply, and sender-name change.

## Data

The plugin contains only Markdown and JSON. It runs no code on your computer and stores nothing itself.

When you use it, Claude sends your requests to your Robotomail account at `robotomail.com` through the connector: search terms, message IDs, and the recipients, subject, and body of any email you send. Robotomail returns mailbox details and message content. No data goes anywhere else.

See the [Robotomail privacy policy](https://robotomail.com/privacy) for how Robotomail handles your data.

## Support

- Documentation: https://robotomail.com/docs/mcp
- Support: support@robotomail.com

## License

MIT. See [LICENSE](LICENSE).
