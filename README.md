# soft-mornings

`soft-mornings-kit`: a small Claude plugin marketplace for morning-routine skills.

| Plugin | What |
|--------|------|
| [email-digest](plugins/email-digest/README.md) | Weekday morning digest of your company Gmail, posted as a Slack DM |
| [writing-training-reports](plugins/writing-training-reports/README.md) | Daily or weekly training report emails saved as a Gmail draft |

## Claude Code (CLI, desktop Code tab, IDE)

```
/plugin marketplace add GraphicDThanh/soft-mornings
/plugin install email-digest@soft-mornings-kit
/plugin install writing-training-reports@soft-mornings-kit
```

Update later with `/plugin marketplace update soft-mornings-kit`.

## claude.ai (chat, desktop Chat tab)

Zip the skill folder and upload it in Settings → Capabilities → Skills:

```bash
cd plugins/email-digest/skills && zip -r ~/Desktop/email-digest.zip email-digest
```

Re-upload after each update; claude.ai doesn't pull new versions.

## Requirements

Gmail connector (both). Slack connector (optional, email-digest).
