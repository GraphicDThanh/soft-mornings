---
name: writing-training-reports
description: Writes daily or weekly training report emails (subject [team][training] YYYYMMDD plus hashtags) from the user's notes and saves them as a Gmail draft. Use for a training report, daily or weekly report, training log, or training progress notes.
---

# Writing training reports

## Profile

Take the `Training report profile` block from the first source that has one: chat, project instructions, preferences, memory. Missing or incomplete → ask all gaps in one message, profile fields only, never the day's work. Ask the team prefix as free text (e.g. `team`); never assume it. When complete, show the full block (no TODOs) and ask "Save this profile to memory?". On "ok" save it with your memory tool, or, with none, tell the user to paste it into preferences or project instructions. "update my profile" repeats this.

```
Training report profile
- Sender: <full name>
- Team prefix: <free text, e.g. team>
- Supporters (To): <greeting name> <email>, ...   (greeting name as in "Hi ...", e.g. Xuan)
- CC: <email>, ...   (e.g. the training group)
- Course: [<name>](<link>)
- Hashtags: #<tag> #<tag>
- Repo: [<repo-name>](<repo link>), folder <folder>
```

## Workflow

- **Notes**: merge into the running report (no duplicates, key points only). Reply in 1–2 lines: what you added, plus missing fields as one numbered list. "show report" → print it.
- **"write" / "draft it"**: fill gaps (branch, commit, day tags), build from [references/template.md](references/template.md), check the Rules, show subject, To, CC, then the body as rendered Markdown (never in a code block, so copy-paste keeps bullets and links). Apply edits, then create the Gmail draft after the user confirms ("just draft it" skips confirmation).
- **Edit after drafting**: update the same draft.

**Coaching**: content that breaks a ★ rule → say plainly what is weak ("'learned caching' doesn't show what you learned") and ask at most 3 specific questions in one message. For plan sub-tasks, lesson ranges, or missing links, propose a concrete answer (e.g. "Lessons 1–4 + Notion note?") so "ok" accepts it. Never propose takeaways from titles; ask what the user learned or offer to shape their own notes. Add only what the user answers or accepts. "draft as is" → stop asking.

## Rules

- Subject: `[<team prefix>][training] YYYYMMDD #tags`, date = today. Weekly: ask the date range, use its last working day, add `#weekly`, open with "This week, I learned/continued…".
- CC always includes every CC address in the profile (e.g. the training group).
- ★ Finished item: task, issue link if any, 2–4 reusable takeaways (what + why/how). "Caching: TTL for lists, invalidate on write", not "Learned caching".
- ★ Include references (notes, docs, board, demo) when they exist.
- ★ Next plan: each item names a task and its sub-tasks. Reject "continue working on practice".
- ★ Issue: title + link, or what / where / error / tried, ending with the help needed.
- Every URL is a Markdown link. Build issue, branch, and commit links from the repo URL pattern; unknown host → ask.
- Omit empty sections and sub-groups.
- Never invent. Missing hash or link → ask; still missing → `<TODO: ...>` and say so.
- Never include secrets (passwords, tokens, keys, `.env` values) or customer data; drop them and tell the user.
- ★ Length: every sentence, bullet, and takeaway ≤100 characters. Over → cut to the key point or split. Check each line before showing the report.
- Tone: slightly formal, concise, clear without context. Sign "Best regards," + sender name only. Never reuse names from [example.md](example.md).

## Gmail draft

ToolSearch `gmail draft`, then `create_draft` with `to`, `cc`, `subject`, `htmlBody` (`<a href>`, nested `<ul><li>`, `<b>` headers), text identical to the approved report. **Never send.** Gmail missing or failing → show the body as rendered Markdown, say to select the formatted text and copy it (the code-block Copy button gives raw Markdown), and give one line why (connect via Settings → Connectors).

## Future expansion (not built)

A full version would need:

- Template, with custom templates allowed.
- Scan Claude sessions (local first).
- Check which MCPs/plugins were called in the day's sessions.
- Write the report from the scan.
