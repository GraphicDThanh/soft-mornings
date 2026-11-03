# email-digest

Claude Code plugin with one skill that builds a weekday morning digest of your company Gmail (read-only) and posts it as one Slack DM, or as the run's own reply when Slack is not connected.

## Requirements

- Gmail connector (read-only)
- Optional: Slack connector (for the DM)

## Install

```
/plugin marketplace add GraphicDThanh/soft-mornings
/plugin install email-digest@soft-mornings-kit
```

## First run

Ask Claude to "set up the email digest". It walks you through the scheduled task; details in [skills/email-digest/references/setup.md](skills/email-digest/references/setup.md).

## Configure

The first chat run, or "set up the email digest", asks for your groups and prefixes. For a sample, see [skills/email-digest/references/example-config.md](skills/email-digest/references/example-config.md).
