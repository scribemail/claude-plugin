# Scribe Mail plugin for Claude

Manage your company's email signatures from Claude. This plugin connects Claude Code and
Cowork to your [Scribe](https://www.scribe-mail.com) workspace and adds the workflow knowledge
to use it well: author and publish signature templates, roll them out to the right teammates,
run signature marketing campaigns, and read engagement analytics.

## Install

```bash
claude plugin marketplace add scribemail/claude-plugin
claude plugin install scribe-mail@scribe-mail
```

On first use Claude opens the Scribe sign-in in your browser. Authentication is OAuth 2.0 via
WorkOS AuthKit. **No API key is pasted anywhere**, and the session acts as you, in your own
workspace, with your own permissions.

## What it adds

**The Scribe MCP server** (`https://mcp.scribe-mail.com/mcp`): 60+ tools covering signature
templates and variants, teammates, emails, smart fields, folders, assets, integrations,
recipients and installations, marketing campaigns, analytics, and the Scribe help center.

**Seven skills** that carry the workflows an agent otherwise gets wrong:

| Skill                       | Covers                                                                                                                                     |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| `signature-authoring`       | The draft → preview → publish → install loop, the block-tree content format, smart fields, reply/internal variants                         |
| `signature-rollout`         | Manual recipients vs. condition rules vs. org-unit targeting vs. future-email auto-assign, and how they stack                              |
| `signature-troubleshooting` | Why a signature is missing, stale, or wrong, in the order that finds the cause fastest                                                     |
| `marketing-campaigns`       | Banner content, targeting, the draft → schedule → pause → resume lifecycle                                                                 |
| `signature-analytics`       | Views, clicks, clickthrough rate, conversion events, visitors; timeseries vs. breakdown                                                    |
| `workspace-audit`           | A one-pass health sweep: no-signature teammates, failed installs, erroring integrations, unpublished drafts                                |
| `teammate-data`             | Bulk smart-field edits, people and aliases, field definitions, and which writes silently do nothing because an integration owns the field |

## Try it

```
Which teammates are missing an email signature?
Audit our Scribe workspace and tell me what to fix first.
Create a signature template for the sales team and show me a preview.
Why isn't ana@acme.com's signature showing up in Outlook?
Show me signature clickthrough by country for the last 30 days.
Launch a campaign banner for our user conference, running 1–15 October.
```

## Safety

Reads run freely. Every write (creating, publishing, installing, assigning, scheduling,
deleting) is confirmed with you first, because it changes what goes out on real company email.
Publishing a template is the moment it reaches mailboxes; the skills preview before they
publish, every time.

## Requirements

- A [Scribe](https://www.scribe-mail.com) workspace, and an owner or admin account in it
  (signature and analytics scopes ride on those roles).
- Claude Code v2.1.0+, or Cowork.

## Links

- Documentation: <https://help.scribe-mail.com>
- Scribe: <https://www.scribe-mail.com>
- Support: <support@scribe-mail.com>

## License

MIT, see [LICENSE](./LICENSE).
