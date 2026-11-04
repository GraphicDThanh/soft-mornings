# Email digest: Slack message format

Use Slack emoji shortcodes exactly as below. The two divider lines are 85 `-` characters.
As the run's own reply (no Slack), use the same layout with Unicode emoji: 📬 🎯 💼 🫂 📊 (same order as the shortcodes).

```
:mailbox_with_mail: Daily Email Digest | <Ddd, Mon D>[ (Preview)] | <u> updates · <a> actions · <c> training reports

-------------------------------------------------------------------------------------

:dart: Needs Attention (<count>)
• <gist> - <sender> · [open](<viewUrl>)

:briefcase: Project Updates (<count>)
• <gist> - <sender> · [open](<viewUrl>)
_+<N> more_

:people_hugging: My People (<count>)
• <gist> - <sender> · [open](<viewUrl>)
• Your report: <gist> - you · [open](<viewUrl>)

:bar_chart: Training Pulse | <c> Reports

Issues (<count>)
• <blocker, question, waiting item, or issue> - <sender> · [open](<viewUrl>)
• <your issue> - you · [open](<viewUrl>)

Current Focus
• <theme>: <n>

Milestones
• <sender> - <milestone>
-------------------------------------------------------------------------------------
🍀 End of digest. <closing>
```

- Never use an em dash (`—`) anywhere in the message; use ` - ` between what and who.
- `[open](<viewUrl>)` is the last thing on an item line.
- Title date: scheduled run → today (e.g. `Tue, Nov 3`). Manual run with `end` = now → the
  next weekday's date plus ` (Preview)`.
- Counts (on the title line): `u` = 🫂 items (incl. the user's own report line), `a` = 🎯
  items (incl. ⏳), `c` = pulse reports (not the user's own).
  Singular for 1 ("1 action"). Drop a part that is 0, and its ` | ` if all are 0. A hidden
  section counts as 0, so its part is dropped (e.g. no "training reports" when 📊 is off).
- 🎯 Needs Attention = approvals and admin, then the ⏳ items as plain `•` lines (no
  separate heading or prefix). Training Pulse holds three lists, in order: Issues (the 🙋 + 🧩
  lists, see 📊 in Step 2), Current Focus, Milestones.
- Current Focus: the 3–5 themes, biggest first, `<theme>: <count>`. Milestones: at most 3,
  `<sender> - <milestone>`.
- No line ends with a period, except the closing line.
- Max items per section from Config, then `_+N more_`. Hide empty sections and empty
  Issues / Current Focus / Milestones lists (no "nothing today" lines).
- Every section empty → title line, `Nothing new since <Ddd, Mon D HH:MM>` (the window
  `start`), closing line.
- `<closing>`: pick by the title date's weekday, so each weekday has its own line and the set
  repeats every week:

  | Day | Closing |
  | --- | --- |
  | Mon | Have a strong start to the week! |
  | Tue | Have a productive day! |
  | Wed | Halfway there, keep it going! |
  | Thu | One more push before Friday! |
  | Fri | Finish strong and enjoy the weekend! |
